MATCH (p1:Persona)-[:AMIGO_DE*2]-(p2:Persona)
WHERE p1 <> p2 
  AND NOT (p1)-[:AMIGO_DE]-(p2)
RETURN DISTINCT p1.nombre AS Persona1, p2.nombre AS Persona2