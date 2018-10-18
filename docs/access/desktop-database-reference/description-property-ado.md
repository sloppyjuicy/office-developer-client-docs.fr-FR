---
<<<<<<< Titre tête : TOCTitle Description propriété (ADO) : Description propriété (ADO) === titre : Description, propriété (ADO) TOCTitle : Description, propriété (ADO)
>>>>>>> Master ms:assetid : 31df5e36-641c-d213-31fc-6244e2983327 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249092(v=office.15) ms:contentKeyID : ms.date 48544064 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="description-property-ado"></a>Description, propriété (ADO)
=======
# <a name="description-property-ado"></a>Description, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Décrit un objet [Error](error-object-ado.md).

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie une valeur de type **String** qui contient une description de l'erreur.

## <a name="remarks"></a>Notes

Utilisez la propriété **Description** pour obtenir une courte description de l'erreur. Affichez cette propriété pour avertir l'utilisateur d'une erreur que vous ne pouvez pas ou ne souhaitez pas gérer. La chaîne provient d'ADO ou d'un fournisseur.

Les fournisseurs sont chargés de transmettre un texte d'erreur spécifique à ADO. ADO ajoute un objet [Error](error-object-ado.md) à la collection **Errors** pour chaque erreur ou avertissement de fournisseur reçu. Énumérez la collection **Errors** pour identifier les erreurs transmises par le fournisseur.

