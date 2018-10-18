---
<<<<<<< Titre tête : TOCTitle Direction propriété (ADO) : Direction propriété (ADO) === titre : Direction, propriété (ADO) TOCTitle : Direction, propriété (ADO)
>>>>>>> Master ms:assetid : 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID : ms.date 48544823 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="direction-property-ado"></a>Direction, propriété (ADO)
=======
# <a name="direction-property-ado"></a>Direction, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique si l'objet [Parameter](parameter-object-ado.md) représente un paramètre d'entrée, de sortie, d'entrée et de sortie, ou encore si le paramètre est la valeur renvoyée par une procédure stockée.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur [ParameterDirectionEnum](parameterdirectionenum.md).

## <a name="remarks"></a>Notes

Utilisez la propriété **Direction** pour spécifier le mode de transmission d'un paramètre dans une procédure. La propriété **Direction** est en lecture-écriture, ce qui vous permet d'utiliser des fournisseurs qui ne retournent pas ces informations ou de définir ces informations lorsque vous ne souhaitez pas qu'ADO effectue un appel supplémentaire au fournisseur pour récupérer des informations de paramètre.

Les fournisseurs ne peuvent pas tous déterminer la direction des paramètres dans leurs procédures stockées. En pareil cas, vous devez définir la propriété **Direction** avant d'exécuter la requête.

