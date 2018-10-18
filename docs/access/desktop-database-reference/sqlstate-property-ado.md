---
<<<<<<< Titre tête : TOCTitle SQLState propriété (ADO) : propriété SQLState (ADO) === titre : SQLSTATE, propriété (ADO) TOCTitle : SQLSTATE, propriété (ADO)
>>>>>>> Master ms:assetid : cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID : ms.date 48547806 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="sqlstate-property-ado"></a>SQLState, propriété (ADO)
=======
# <a name="sqlstate-property-ado"></a>SQLSTATE, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique l'état SQL d'un objet [Error](error-object-ado.md) donné.

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie une valeur **String** de 5 caractères qui, conformément à la norme ANSI SQL, indique le code d'erreur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **SQLState** pour lire le code d'erreur à 5 caractères renvoyé par le fournisseur lorsqu'une erreur se produit lors du traitement d'une instruction SQL. Par exemple, lorsque l'on utilise le fournisseur Microsoft OLE DB pour ODBC avec une base de données Microsoft SQL Server, les codes d'erreur d'état SQL sont issus d'ODBC ; ils reposent soit sur des erreurs spécifiques à ODBC, soit sur des erreurs provenant de Microsoft SQL Server, et sont ensuite mappés sur des erreurs ODBC. Ces codes d'erreur sont documentés dans la norme ANSI SQL, mais peuvent être implémentés différemment dans d'autres sources de données.

