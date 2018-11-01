---
title: Wrappers de classe Java ADO
TOCTitle: ADO Java Class Wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 602d3407d78843331fdb78ef728cebbc69bace14
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889461"
---
# <a name="ado-java-class-wrappers"></a><span data-ttu-id="de7b4-102">Wrappers de classe Java ADO</span><span class="sxs-lookup"><span data-stu-id="de7b4-102">ADO Java Class Wrappers</span></span>


<span data-ttu-id="de7b4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de7b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de7b4-p101">Ce code déclare une instance du wrapper de la classe [Recordset](recordset-object-ado.md) ADO et initialise le tout sur la même ligne de code. En outre, il déclare des variables pour chacun des arguments de la méthode [Open](open-method-ado-recordset.md), en particulier pour [LockType](locktype-property-ado.md) et [CursorType](cursortype-property-ado.md) (car Java ne prend pas en charge les types énumérés). Il ouvre et ferme l'objet **Recordset**. L'affectation de la valeur NULL à Rs1 prévoit simplement la libération de la variable lorsque Java procède à sa libération systématique et intermittente des objets inutilisés.</span><span class="sxs-lookup"><span data-stu-id="de7b4-p101">This code declares an instance of the ADO [Recordset](recordset-object-ado.md) class wrapper and initializes it, all on the same line of code. Further, it declares variables for each of the arguments in the [Open](open-method-ado-recordset.md) method, especially for [LockType](locktype-property-ado.md) and [CursorType](cursortype-property-ado.md) (because Java doesn't support enumerated types). It opens and closes the **Recordset** object. Setting Rs1 to NULL merely schedules that variable to be released when Java performs its systematic and intermittent release of unused objects.</span></span>

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

