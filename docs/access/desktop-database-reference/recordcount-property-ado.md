---
<<<<<<< Titre tête : TOCTitle de la propriété RecordCount (ADO) : propriété RecordCount (ADO) === titre : RecordCount, propriété (ADO) TOCTitle : RecordCount, propriété (ADO)
>>>>>>> Master ms:assetid : e3072d10-5bf7-02a8-027e-a9d9a34e3f27 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250155(v=office.15) ms:contentKeyID : ms.date 48548304 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="recordcount-property-ado"></a>RecordCount, propriété (ADO)
=======
# <a name="recordcount-property-ado"></a>RecordCount, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le nombre d'enregistrements dans un objet [Recordset](recordset-object-ado.md).

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Retourne une valeur de type **Long** qui indique le nombre d'enregistrements dans le **Recordset**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **RecordCount** pour connaître le nombre d'enregistrements dans un objet **Recordset**. La propriété renvoie -1 quand ADO ne parvient pas à déterminer le nombre d'enregistrements ou si le fournisseur (ou le type de cursor) ne prend pas en charge la propriété **RecordCount**. Les tentatives de lecture de la propriété **RecordCount** sur un **Recordset** fermé génèrent une erreur.

Si l'objet **Recordset** prend en charge le positionnement approximatif ou les signets (c'est-à-dire si **Supports (adApproxPosition)** ou **Supports (adBookmark)**, respectivement, renvoient la valeur **True** ) cette valeur est égale au nombre exact d'enregistrements dans le **Recordset**, qu'il soit complet ou non. Si l'objet **Recordset** ne prend pas en charge le positionnement approximatif, il se peut que cette propriété représente une charge significative pour les ressources, car tous les enregistrements devront être récupérés et comptés pour qu'une valeur **RecordCount** précise puisse être renvoyée.

Le type de curseur de l'objet **Recordset** détermine si les enregistrements pourront ou ne pourront pas être comptés. La propriété **RecordCount** renvoie -1 si le curseur est de type avant uniquement. Elle renvoie le nombre réel d'enregistrements si le curseur est statique ou basé sur un jeu de clé et -1 ou soit le nombre d'enregistrements si le curseur est dynamique (cela dépend alors de la source de données).

