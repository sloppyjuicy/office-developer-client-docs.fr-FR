---
title: Field2.Expression, propriété (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292817"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="b2903-102">Field2.Expression, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="b2903-102">Field2.Expression property (DAO)</span></span>

<span data-ttu-id="b2903-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2903-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2903-104">Obtient ou définit une expression qui représente la formule d’un champ calculé.</span><span class="sxs-lookup"><span data-stu-id="b2903-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="b2903-105">**String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b2903-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="b2903-106">Informations de version</span><span class="sxs-lookup"><span data-stu-id="b2903-106">Version information</span></span>

<span data-ttu-id="b2903-107">Version ajoutée : Access 2010</span><span class="sxs-lookup"><span data-stu-id="b2903-107">Version added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="b2903-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2903-108">Syntax</span></span>

<span data-ttu-id="b2903-109">*.* Expression</span><span class="sxs-lookup"><span data-stu-id="b2903-109">*expression* .Expression</span></span>

<span data-ttu-id="b2903-110">*expression* une variable qui représente une **champ2** objet.</span><span class="sxs-lookup"><span data-stu-id="b2903-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2903-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2903-111">Remarks</span></span>

<span data-ttu-id="b2903-112">Dans Access 2013, vous pouvez créer des champs de table qui calculent des valeurs.</span><span class="sxs-lookup"><span data-stu-id="b2903-112">In Access 2013, you can create table fields that calculate values.</span></span> <span data-ttu-id="b2903-113">Les calculs peuvent inclure des valeurs provenant de champs de la même table, ainsi que des fonctions Access intégrées.</span><span class="sxs-lookup"><span data-stu-id="b2903-113">The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="b2903-114">Le calcul ne peut pas inclure de champs provenant d’autres tables ou requêtes.</span><span class="sxs-lookup"><span data-stu-id="b2903-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="b2903-115">Les résultats du calcul sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b2903-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="b2903-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="b2903-116">Example</span></span>

<span data-ttu-id="b2903-p103">L'exemple suivant montre comment créer un champ calculé. La méthode CreateField crée un champ nommé **FullName**. La propriété Expression est ensuite définie sur l'expression qui calcule la valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="b2903-p103">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="b2903-120">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="b2903-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

