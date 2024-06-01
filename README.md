import matplotlib.pyplot as plt
import networkx as nx

# Crear el grafo
G = nx.DiGraph()

# Agregar nodos y relaciones
G.add_node("Estudio: Participación de Mujeres Indígenas en la Economía de Petalcingo")
G.add_node("Afecta Dinámicas de Género en Comunidades Rurales")
G.add_node("Actividades Económicas")
G.add_node("Agricultura")
G.add_node("Artesanía")
G.add_node("Comercio")
G.add_node("Cooperativas")
G.add_node("Histórico: Roles Tradicionales")
G.add_node("Limitación de Oportunidades Económicas")
G.add_node("Dependencia de los Hombres")
G.add_node("Cambios en Dinámicas de Género y Territoriales desde 2010")
G.add_node("Identificación de Cambios, Desafíos y Oportunidades")

# Agregar aristas
G.add_edges_from([
    ("Estudio: Participación de Mujeres Indígenas en la Economía de Petalcingo", "Afecta Dinámicas de Género en Comunidades Rurales"),
    ("Afecta Dinámicas de Género en Comunidades Rurales", "Actividades Económicas"),
    ("Actividades Económicas", "Agricultura"),
    ("Actividades Económicas", "Artesanía"),
    ("Actividades Económicas", "Comercio"),
    ("Actividades Económicas", "Cooperativas"),
    ("Estudio: Participación de Mujeres Indígenas en la Economía de Petalcingo", "Histórico: Roles Tradicionales"),
    ("Histórico: Roles Tradicionales", "Limitación de Oportunidades Económicas"),
    ("Limitación de Oportunidades Económicas", "Dependencia de los Hombres"),
    ("Estudio: Participación de Mujeres Indígenas en la Economía de Petalcingo", "Cambios en Dinámicas de Género y Territoriales desde 2010"),
    ("Cambios en Dinámicas de Género y Territoriales desde 2010", "Identificación de Cambios, Desafíos y Oportunidades")
])

# Dibujar el grafo
plt.figure(figsize=(12, 8))
pos = nx.spring_layout(G)
nx.draw(G, pos, with_labels=True, node_color="skyblue", node_size=3000, font_size=10, font_weight="bold", edge_color="gray")
plt.title("Diagrama de Participación de Mujeres Indígenas en la Economía de Petalcingo")
plt.show()
