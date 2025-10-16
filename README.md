## Diagramma delle classi — Sistema scolastico

```mermaid
%%{init: {'theme': 'base', 'themeVariables': {
    'primaryTextColor': '#423E28',
    'primaryColor': '#86DEB7',
    'lineColor': '#ADEEE3',
    'fontSize': '16px'
}}}%%

classDiagram
    class Persona {
        - string nome
        - string cognome
        + void saluta()
    }

    class Studente {
        - int matricola
        + void studia()
    }

    class Insegnante {
        - string materia
        + void insegna()
    }

    Persona <|-- Studente : eredita
    Persona <|-- Insegnante : eredita

    note for Persona "Classe base astratta che rappresenta una persona nella scuola"
    note for Studente "Ogni studente ha una matricola univoca"
    note for Insegnante "Gli insegnanti hanno una materia di competenza"
