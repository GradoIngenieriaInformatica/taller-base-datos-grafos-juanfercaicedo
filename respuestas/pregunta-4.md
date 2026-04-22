MATCH (p:Persona)-[:VIVE_EN]->(c:Ciudad)
WITH c.nombre AS ciudad, count(p) AS cantidad_personas
WHERE cantidad_personas > 2
RETURN ciudad, cantidad_personas