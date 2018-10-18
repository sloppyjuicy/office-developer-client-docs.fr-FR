---
<<<<<<< Titre tête : TOCTitle NativeError propriété (ADO) : NativeError propriété (ADO) === titre : NativeError, propriété (ADO) TOCTitle : NativeError, propriété (ADO)
>>>>>>> Master ms:assetid : 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b ms:mtpsurl : https://msdn.microsoft.com/library/JJ249731(v=office.15) ms:contentKeyID : ms.date 48546685 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="nativeerror-property-ado"></a>NativeError, propriété (ADO)
=======
# <a name="nativeerror-property-ado"></a>NativeError, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le code d'erreur spécifique au fournisseur pour un objet [Error](error-object-ado.md) donné.

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie une valeur de type **Long** qui indique le code d'erreur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **NativeError** pour récupérer les informations spécifiques à la base de données sur l'objet **Error** concerné. Par exemple, lorsque l'on utilise un fournisseur Microsoft ODBC pour OLE DB avec une base de données Microsoft SQL, les codes d'erreur d'origine provenant de SQL Server transitent par ODBC et par le fournisseur ODBC pour atteindre la propriété **Native Error** ADO.

