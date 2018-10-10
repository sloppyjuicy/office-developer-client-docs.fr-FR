---
title: Transformation (référence du bureau de la base de données Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be9e0f8e017e91152ed876b933e0c0c01a7f355e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472576"
---
# <a name="reshaping"></a><span data-ttu-id="72184-102">Modification de la mise en forme</span><span class="sxs-lookup"><span data-stu-id="72184-102">Reshaping</span></span>


<span data-ttu-id="72184-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="72184-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72184-p101">Un objet **Recordset** créé par une clause d’une commande de mise en forme peut recevoir un *alias* (généralement assorti du mot-clé AS). L’alias d’un objet **Recordset** mis en forme peut être référencé dans une commande totalement différente. En d’autres termes, vous pouvez réutiliser, c’est-à-dire *modifier la mise en forme* d’un objet **Recordset** préalablement mis en forme dans une nouvelle commande de mise en forme. Pour prendre en charge cette fonctionnalité, ADO propose une propriété nommée [Reshape Name](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="72184-p101">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword). The alias of a shaped **Recordset** can be referenced in an entirely different command. That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command. To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="72184-p102">La fonctionnalité de modification de la mise en forme s'avère utile dans deux cas. En premier lieu, elle permet d'associer un objet **Recordset** existant à un nouvel objet **Recordset** parent.</span><span class="sxs-lookup"><span data-stu-id="72184-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="72184-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="72184-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="72184-111">La deuxième fonction consiste à activer l’accès non hiérarchisé aux objets **Recordset** enfants existants, à l’aide de la syntaxe `"SHAPE <recordset reshape name>"`.</span><span class="sxs-lookup"><span data-stu-id="72184-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>


> [!NOTE]
> <P><span data-ttu-id="72184-p103">[!REMARQUE] Vous ne pouvez pas ajouter de colonnes à un objet <STRONG>Recordset</STRONG> existant, ni modifier la mise en forme d'un objet <STRONG>Recordset</STRONG> paramétré ou des objets <STRONG>Recordset</STRONG> spécifiés dans une clause COMPUTE intermédiaire, ni exécuter des opérations d'agrégation sur un objet <STRONG>Recordset</STRONG> descendant de l'objet <STRONG>Recordset</STRONG> dont la mise en forme a été modifiée. L'objet <STRONG>Recordset</STRONG> visé par l'opération de modification de la mise en forme et la nouvelle commande de mise en forme doivent tous deux utiliser le même objet <A href="connection-object-ado.md">Connection</A>.</span><span class="sxs-lookup"><span data-stu-id="72184-p103">You cannot append columns to an existing <STRONG>Recordset</STRONG>, reshape a parameterized <STRONG>Recordset</STRONG> or the <STRONG>Recordset</STRONG> objects in any intervening COMPUTE clause, or perform aggregate operations on any <STRONG>Recordset</STRONG> descendant from the <STRONG>Recordset</STRONG> being reshaped. The <STRONG>Recordset</STRONG> being reshaped and the new shape command must both use the same <A href="connection-object-ado.md">Connection</A>.</span></span></P>


