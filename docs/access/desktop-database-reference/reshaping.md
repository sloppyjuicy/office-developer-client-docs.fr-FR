---
title: Transformation (référence du bureau de la base de données Access)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49a61e72a4d9260b73275d84ce912ebc76f37652
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996453"
---
# <a name="reshaping"></a><span data-ttu-id="cd6ca-102">Remise en forme</span><span class="sxs-lookup"><span data-stu-id="cd6ca-102">Reshaping</span></span>

<span data-ttu-id="cd6ca-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd6ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd6ca-p101">Un objet **Recordset** créé par une clause d’une commande de mise en forme peut recevoir un *alias* (généralement assorti du mot-clé AS). L’alias d’un objet **Recordset** mis en forme peut être référencé dans une commande totalement différente. En d’autres termes, vous pouvez réutiliser, c’est-à-dire *modifier la mise en forme* d’un objet **Recordset** préalablement mis en forme dans une nouvelle commande de mise en forme. Pour prendre en charge cette fonctionnalité, ADO propose une propriété nommée [Reshape Name](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cd6ca-p101">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword). The alias of a shaped **Recordset** can be referenced in an entirely different command. That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command. To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="cd6ca-p102">La fonctionnalité de modification de la mise en forme s'avère utile dans deux cas. En premier lieu, elle permet d'associer un objet **Recordset** existant à un nouvel objet **Recordset** parent.</span><span class="sxs-lookup"><span data-stu-id="cd6ca-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="cd6ca-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="cd6ca-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="cd6ca-111">La deuxième fonction consiste à activer l’accès non hiérarchisé aux objets **Recordset** enfants existants, à l’aide de la syntaxe `"SHAPE <recordset reshape name>"`.</span><span class="sxs-lookup"><span data-stu-id="cd6ca-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="cd6ca-112">[!REMARQUE] Vous ne pouvez pas ajouter de colonnes à un objet **Recordset** existant, ni modifier la mise en forme d'un objet **Recordset** paramétré ou des objets **Recordset** spécifiés dans une clause COMPUTE intermédiaire, ni exécuter des opérations d'agrégation sur un objet **Recordset** descendant de l'objet **Recordset** dont la mise en forme a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="cd6ca-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="cd6ca-113">Le **jeu d’enregistrements** en cours remodelée et la nouvelle forme commande doivent tous deux utiliser le même \*\* objet[Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="cd6ca-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


