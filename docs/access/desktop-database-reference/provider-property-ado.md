---
<<<<<<< Titre tête : TOCTitle fournisseur propriété (ADO) : fournisseur de propriété (ADO) === titre : propriété Provider (ADO) TOCTitle : propriété Provider (ADO)
>>>>>>> Master ms:assetid : 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl : https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID : ms.date 48543543 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="provider-property-ado"></a>Provider, propriété (ADO)
=======
# <a name="provider-property-ado"></a>Propriété Provider (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le nom du fournisseur d'un objet [Connection](connection-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur **String** qui indique le nom du fournisseur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Provider** pour définir ou renvoyer le nom du fournisseur d’une connexion. Cette propriété peut aussi être définie par le contenu de la propriété [ConnectionString](connectionstring-property-ado.md) ou de l’argument *ConnectionString* de la méthode [Open](open-method-ado-connection.md). Toutefois, si l’on indique le fournisseur à plusieurs endroits et que l’on appelle la méthode **Open**, les résultats sont imprévisibles. Si aucun fournisseur n’est spécifié, la valeur par défaut de la propriété est MSDASQL ([Fournisseur Microsoft OLE DB pour ODBC](microsoft-ole-db-provider-for-odbc.md)).

La propriété **Provider** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte. Le paramètre ne prend que lorsque l'on ouvre l'objet **Connection** ou que l'on accède à la collection [Properties](properties-collection-ado.md) de l'objet **Connection**. Si le paramètre n'est pas valide, une erreur est générée.

