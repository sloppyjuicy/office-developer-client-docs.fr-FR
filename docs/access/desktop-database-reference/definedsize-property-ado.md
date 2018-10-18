---
<<<<<<< Titre tête : TOCTitle de la propriété DefinedSize (ADO) : propriété DefinedSize (ADO) === titre : DefinedSize, propriété (ADO) TOCTitle : DefinedSize, propriété (ADO)
>>>>>>> Master ms:assetid : 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID : ms.date 48546257 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="definedsize-property-ado"></a>DefinedSize, propriété (ADO)
=======
# <a name="definedsize-property-ado"></a>DefinedSize, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique la capacité en données d'un objet [Field](field-object-ado.md).

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie une valeur de type **Long** qui reflète la taille définie pour un champ sous la forme d'un nombre d'octets.

## <a name="remarks"></a>Notes

Utilisez la propriété **DefinedSize** pour déterminer la capacité en données d'un objet **Field**.

Les propriétés **DefinedSize** et [ActualSize](actualsize-property-ado.md) sont différentes. Par exemple, imaginez un objet **Field** avec le type déclaré **adVarChar** et une propriété **DefinedSize** de 50, contenant un caractère unique. La valeur retournée pour la propriété **ActualSize** correspond à la longueur en octets du caractère unique.

