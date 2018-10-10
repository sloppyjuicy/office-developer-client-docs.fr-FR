---
title: Wrappers de classe Java ADO
TOCTitle: ADO Java Class Wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa3a4d1d2a917997b9e7ed5407d4f2ce8d1d0361
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471232"
---
# <a name="ado-java-class-wrappers"></a>Wrappers de classe Java ADO


**S’applique à**: Access 2013 | Office 2013

Ce code déclare une instance du wrapper de la classe [Recordset](recordset-object-ado.md) ADO et initialise le tout sur la même ligne de code. En outre, il déclare des variables pour chacun des arguments de la méthode [Open](open-method-ado-recordset.md), en particulier pour [LockType](locktype-property-ado.md) et [CursorType](cursortype-property-ado.md) (car Java ne prend pas en charge les types énumérés). Il ouvre et ferme l'objet **Recordset**. L'affectation de la valeur NULL à Rs1 prévoit simplement la libération de la variable lorsque Java procède à sa libération systématique et intermittente des objets inutilisés.

```java 
 
public static void main( String args[]) 
{ 
 msado15._Recordset Rs1 = new msado15.Recordset(); 
 Variant Source = new Variant( "SELECT * FROM Authors" ); 
 Variant Connect = new Variant( "DSN=AdoDemo;UID=admin;PWD=;" ); 
 int LockType = msado15.CursorTypeEnum.adOpenForwardOnly; 
 int CursorType = msado15.LockTypeEnum.adLockReadOnly; 
 int Options = -1; 
 
 Rs1.Open( Source, Connect, LockType, CursorType, Options ); 
 Rs1.Close(); 
 Rs1 = null; 
 
 System.out.println( "Success!\n" ); 
} 
```

