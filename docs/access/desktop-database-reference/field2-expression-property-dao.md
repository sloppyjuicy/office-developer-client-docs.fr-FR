---
title: Propriété Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720085"
---
# <a name="field2expression-property-dao"></a><span data-ttu-id="3c200-102">Propriété Field2.Expression (DAO)</span><span class="sxs-lookup"><span data-stu-id="3c200-102">Field2.Expression property (DAO)</span></span>

<span data-ttu-id="3c200-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c200-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c200-104">Obtient ou définit une expression qui représente la formule pour un champ calculé.</span><span class="sxs-lookup"><span data-stu-id="3c200-104">Gets or sets an expression that represents the formula for a calculated field.</span></span> <span data-ttu-id="3c200-105">**String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3c200-105">Read/write **String**.</span></span>

## <a name="version-information"></a><span data-ttu-id="3c200-106">Informations de version</span><span class="sxs-lookup"><span data-stu-id="3c200-106">Version information</span></span>

<span data-ttu-id="3c200-107">Version ajoutée : Access 2010</span><span class="sxs-lookup"><span data-stu-id="3c200-107">Version added: Access 2010</span></span>

## <a name="syntax"></a><span data-ttu-id="3c200-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c200-108">Syntax</span></span>

<span data-ttu-id="3c200-109">*expression* . Expression</span><span class="sxs-lookup"><span data-stu-id="3c200-109">*expression* .Expression</span></span>

<span data-ttu-id="3c200-110">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="3c200-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c200-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="3c200-111">Remarks</span></span>

<span data-ttu-id="3c200-112">Dans Access 2013, vous pouvez créer des champs de table calculer des valeurs.</span><span class="sxs-lookup"><span data-stu-id="3c200-112">In Access 2013, you can create table fields that calculate values.</span></span> <span data-ttu-id="3c200-113">Les calculs peuvent inclure des valeurs de champs dans la même table, ainsi que les fonctions intégrées Access.</span><span class="sxs-lookup"><span data-stu-id="3c200-113">The calculations can include values from fields in the same table as well as built-in Access functions.</span></span>

<span data-ttu-id="3c200-114">Le calcul ne peut pas inclure de champs à partir d’autres tables ou les requêtes.</span><span class="sxs-lookup"><span data-stu-id="3c200-114">The calculation cannot include fields from other tables or queries.</span></span>

<span data-ttu-id="3c200-115">Les résultats du calcul sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3c200-115">The results of the calculation are read-only.</span></span>

## <a name="example"></a><span data-ttu-id="3c200-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="3c200-116">Example</span></span>

<span data-ttu-id="3c200-p103">L'exemple suivant montre comment créer un champ calculé. La méthode CreateField crée un champ nommé **FullName**. La propriété Expression est ensuite définie sur l'expression qui calcule la valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="3c200-p103">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="3c200-120">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="3c200-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

