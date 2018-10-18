---
<<<<<<< Titre tête : TOCTitle préparé propriété (ADO) : propriété (ADO) préparé === titre : préparé, propriété (ADO) TOCTitle : préparé, propriété (ADO)
>>>>>>> Master ms:assetid : 33becda2-faab-5000-8904-6ffd8c5805f2 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249105(v=office.15) ms:contentKeyID : ms.date 48544116 : 18/09/2015 mtps_version : v=office.15 f1_keywords :
- Ado210.chm1231161 f1_categories :
- Office.Version=v15
---

<<<<<<< Tête
# <a name="prepared-property-ado"></a>Prepared, propriété (ADO)
=======
# <a name="prepared-property-ado"></a>Prepared, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique s'il faut enregistrer la version compilée d'une commande avant exécution.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur **booléenne** qui, si elle est définie sur **True**, indique que la commande doit être préparée.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Prepared** pour que le fournisseur enregistre une version préparée (ou compilée) de la requête spécifiée dans la propriété [CommandText](commandtext-property-ado.md) avant la première exécution d'un objet [Command](command-object-ado.md). Cela risque de ralentir la première exécution de la commande, mais une fois la commande compilée, c'est cette version compilée que le fournisseur utilise lors des exécutions suivantes, ce qui améliore les performances.

Si la valeur de la propriété est **False**, le fournisseur exécute l'objet **Command** directement sans créer de version compilée.

Si le fournisseur ne prend pas en charge la préparation des commandes, il peut renvoyer une erreur dès que la valeur **True** est attribuée à cette propriété. S'il ne renvoie pas d'erreur, il ignore simplement la requête de préparation et attribue la valeur **False** à la propriété **Prepared**.

