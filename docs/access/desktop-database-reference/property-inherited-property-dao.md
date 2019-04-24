---
title: Propriété. Inherited, propriété (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf3aef6d04c7d7cc573ec1d6efaca7d5238f5125
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302925"
---
# <a name="propertyinherited-property-dao"></a>Propriété. Inherited, propriété (DAO)


**S’applique à** : Access 2013, Office 2013 

Renvoie une valeur qui indique si un objet **[Property](property-object-dao.md)** est hérité d'un objet sous-jacent.

## <a name="syntax"></a>Syntaxe

*expression* . Proviennent

*expression* Variable qui représente un objet **Property** .

## <a name="remarks"></a>Remarques

Pour les objets **Property** intégrés qui représentent des propriétés prédéfinies, la seule valeur de retour possible est **False**.

La propriété **Inherited** permet de déterminer si un objet **Property** défini par l'utilisateur a été créé pour l'objet auquel il s'applique ou si l'objet **Property** a été hérité d'un autre objet. Par exemple, supposons que vous créez un nouvel objet **Property** pour un objet **[QueryDef](querydef-object-dao.md)** et que vous ouvrez ensuite un objet **[Recordset](recordset-object-dao.md)** à partir de l'objet **QueryDef**. Ce nouvel objet **Property** fait partie de la collection [**Properties**](properties-collection-dao.md) de l'objet **Recordset** et sa propriété **Inherited** est définie sur **True** car la propriété a été créée pour l'objet **QueryDef** et non pour l'objet **Recordset**.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **Inherited** pour déterminer si un objet **Property** défini par l'utilisateur a été créé pour un objet **Recordset** ou pour un autre objet sous-jacent.

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

