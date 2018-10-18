---
<<<<<<< Titre tête : TOCTitle PageCount propriété (ADO) : PageCount propriété (ADO) === titre : PageCount, propriété (ADO) TOCTitle : PageCount, propriété (ADO)
>>>>>>> Master ms:assetid : 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID : ms.date 48546609 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="pagecount-property-ado"></a>PageCount, propriété (ADO)
=======
# <a name="pagecount-property-ado"></a>PageCount, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le nombre de pages de données que contient l'objet [Recordset](recordset-object-ado.md).

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Retourne une valeur de type **Long** qui indique le nombre de pages dans le **Recordset**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **PageCount** pour déterminer le nombre de pages que contient l'objet **Recordset**. *Les pages* sont des groupes d’enregistrements dont la taille est égale à [la propriété PageSize](pagesize-property-ado.md) . Même si la dernière page est incomplète et que le nombre d'enregistrements qu'elle contient est inférieur à la valeur de **PageSize**, elle est considérée comme une page supplémentaire dans la valeur **PageCount**. Si l'objet **Recordset** ne prend pas en charge cette propriété, la valeur sera -1, pour indiquer que la propriété **PageCount** ne peut pas être déterminée.

Pour plus d'informations sur les fonctionnalités relatives aux pages, voir les propriétés **PageSize** et [AbsolutePage](absolutepage-property-ado.md).

