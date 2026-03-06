# student-report-card-generator-
# Script Python pour saisir les notes d’un élève, calculer la moyenne, attribuer une mention selon des seuils, et afficher un bulletin. Boucle while pour gérer plusieurs élèves successivement.

while True:
    
    student_id = input("ID de l'élève : ")
    name = input("Nom de l'élève : ")
    mark_english = int(input("Note Anglais : "))
    mark_maths = int(input("Note Maths : "))
    mark_biology = int(input("Note Biologie : "))

    
    marks_dict = {
        "Anglais": mark_english,
        "Maths": mark_maths,
        "Biologie": mark_biology
    }

    moyenne = sum(marks_dict.values()) / len(marks_dict)

    if moyenne >= 16:
        grade = "Très Bien"
    elif moyenne >= 12:
        grade = "Bien"
    elif moyenne >= 10:
        grade = "Obtenu"
    else:
        grade = "Insuffisant"

    print("\n--- BULLETIN SCOLAIRE ---")
    print(f"ID : {student_id}")
    print(f"Nom : {name}")
    print(f"Moyenne : {moyenne:.2f}")
    print(f"Mention : {grade}")
    print("-------------------------\n")

    continuer = input("Ajouter un autre élève ? (oui/non) ").lower()
    if continuer != "oui":
        break
