---
<<<<<<< Titre tête : TOCTitle DefaultDatabase propriété (ADO) : propriété DefaultDatabase (ADO) === titre : DefaultDatabase, propriété (ADO) TOCTitle : DefaultDatabase, propriété (ADO)
>>>>>>> Master ms:assetid : a35c5631-f9d9-e51f-950b-e52169830d94 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249757(v=office.15) ms:contentKeyID : ms.date 48546784 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase, propriété (ADO)
=======
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique la base de données par défaut d'un objet [Connection](connection-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **String**, qui correspond au nom d'une base de données disponible du fournisseur.

## <a name="remarks"></a>Notes

Utilisez la propriété **DefaultDatabase** pour définir ou retourner le nom de la base de données par défaut d'un objet **Connection** spécifique.

S'il existe une base de données par défaut, les chaînes SQL peuvent utiliser une syntaxe non qualifiée pour accéder aux objets de cette base de données. Pour accéder aux objets dans une base de données autre que celle spécifiée dans la propriété **DefaultDatabase**, vous devez qualifier les noms d'objet avec le nom de la base de données souhaitée. Lors de la connexion, le fournisseur écrit les informations de la base de données par défaut dans la propriété **DefaultDatabase**. Certains fournisseurs n'autorisent qu'une seule base de données par connexion, auquel cas vous ne pouvez pas modifier la propriété **DefaultDatabase**.

Il se peut que certains fournisseurs et sources de données ne prennent pas en charge cette fonctionnalité et retournent une erreur ou une chaîne vide.

**L’utilisation du Service de données à distance** Cette propriété n’est pas disponible sur un objet de **connexion** côté client.

