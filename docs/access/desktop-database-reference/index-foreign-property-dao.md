---
title: Index.Foreign Property (DAO)
TOCTitle: Foreign Property
ms:assetid: 81272436-a506-4b72-fd28-2d68e76d6d9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196489(v=office.15)
ms:contentKeyID: 48545943
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052974
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 410629c3e5ebec47dd8acefd852379ee74568832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470816"
---
# <a name="indexforeign-property-dao"></a>Index.Foreign Property (DAO)

**S’applique à**: Access 2013 | Office 2013

Renvoie une valeur qui indique si un objet **[Index](index-object-dao.md)** représente une clé étrangère d'une table (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . Étrangère

*expression* Variable qui représente un objet **Index** .

## <a name="remarks"></a>Remarques

La valeur de retour est une donnée de type **Boolean** qui renvoie **True** si l'objet **Index** représente un clé étrangère.

Une clé étrangère consiste en un ou plusieurs champs d'une table étrangère qui identifient de manière unique toutes les lignes d'une table primaire.

Le moteur de base de données Microsoft Access crée un objet **Index** pour la table étrangère et définit la propriété **Foreign** lorsque vous créez une relation qui impose l'intégrité référentielle.

## <a name="example"></a>Exemple

Cet exemple illustre comment la propriété **Foreign** permet d'identifier les objets **Index** d'une **TableDef** faisant office d'index de clé. Ces derniers sont créés par le moteur de base de données Microsoft Access lors de la création d'une **Relation**. Le nom par défaut des index de clés étrangères est le nom de la table primaire suivi de celui de la table étrangère. La fonction ForeignOutput est indispensable pour l'exécution de cette procédure.

```vb
    Sub ForeignX() 
     
     Dim dbsNorthwind As Database 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report on foreign key indexes from two 
     ' TableDef objects and a QueryDef object. 
     ForeignOutput .TableDefs!Products 
     ForeignOutput .TableDefs!Orders 
     ForeignOutput .TableDefs![Order Details] 
     
     .Close 
     End With 
     
    End Sub 
     
    Function ForeignOutput(tdfTemp As TableDef) 
     
     Dim idxLoop As Index 
     
     With tdfTemp 
     Debug.Print "Indexes in " & .Name & " TableDef" 
     ' Enumerate the Indexes collection of the specified 
     ' TableDef object. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Debug.Print " Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     End With 
     
    End Function
```
