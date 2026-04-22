MATCH (p:Persona)-[:AMIGO_DE]-(amigo:Persona)-[:VIVE_EN]->(c:Ciudad)
RETURN p.nombre AS Persona, collect(DISTINCT c.nombre) AS CiudadesDeAmigos