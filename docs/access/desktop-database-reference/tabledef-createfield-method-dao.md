---
title: Méthode TableDef.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 713f2530369a824a6d7204655ded4333f7fe2765
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710432"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="b8cbc-102">Méthode TableDef.CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="b8cbc-102">TableDef.CreateField method (DAO)</span></span>

<span data-ttu-id="b8cbc-103">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8cbc-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="b8cbc-104">Crée un objet **[Field](field-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="b8cbc-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8cbc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8cbc-105">Syntax</span></span>

<span data-ttu-id="b8cbc-106">*expression* . CreateField (_**nom**_, _**Type**_, _**taille**_)</span><span class="sxs-lookup"><span data-stu-id="b8cbc-106">*expression* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span></span>

<span data-ttu-id="b8cbc-107">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="b8cbc-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8cbc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8cbc-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8cbc-109">Nom</span><span class="sxs-lookup"><span data-stu-id="b8cbc-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b8cbc-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="b8cbc-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b8cbc-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="b8cbc-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b8cbc-112">Description</span><span class="sxs-lookup"><span data-stu-id="b8cbc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8cbc-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="b8cbc-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b8cbc-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b8cbc-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b8cbc-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b8cbc-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b8cbc-p101">Chaîne qui identifie de manière unique le nouvel objet <strong>Field</strong>. Reportez-vous à la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour plus d'informations sur les noms valides pour l'objet <strong>Field</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b8cbc-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8cbc-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="b8cbc-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="b8cbc-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b8cbc-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="b8cbc-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b8cbc-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b8cbc-p102">Constante qui détermine le type de données du nouvel objet <strong>Field</strong>. Pour connaître les types de données valides, reportez-vous à la propriété <strong><a href="field-type-property-dao.md">Type</a></strong>.  </span><span class="sxs-lookup"><span data-stu-id="b8cbc-p102">A constant that determines the data type of the new <strong>Field</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8cbc-123"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="b8cbc-123"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="b8cbc-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b8cbc-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="b8cbc-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b8cbc-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b8cbc-126">Integer qui indique la taille maximale, en octets, d'un objet <strong>Field</strong> qui contient du texte.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-126">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text.</span></span> <span data-ttu-id="b8cbc-127">Voir la propriété <strong><a href="field-size-property-dao.md">Size</a></strong> pour les valeurs de taille valide.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-127">See the <strong><a href="field-size-property-dao.md">Size</a></strong> property for valid size values.</span></span> <span data-ttu-id="b8cbc-128">Cet argument est ignoré pour les champs numériques et de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-128">This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="b8cbc-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8cbc-129">Return value</span></span>

<span data-ttu-id="b8cbc-130">Champ</span><span class="sxs-lookup"><span data-stu-id="b8cbc-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="b8cbc-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8cbc-131">Remarks</span></span>

<span data-ttu-id="b8cbc-p104">Vous pouvez utiliser la méthode **CreateField** pour créer un champ, spécifier le nom, le type de données et la taille du champ. Si vous omettez une ou plusieurs des parties facultatives lorsque vous utilisez la méthode **CreateField**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou réinitialiser la propriété correspondante avant d'ajouter le nouvel objet à la collection. Une fois que vous avez ajouté le nouvel objet, vous pouvez modifier une partie de ses paramètres de propriété, mais pas tous. Pour plus d'informations, reportez-vous aux rubriques concernant cette propriété.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-p104">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="b8cbc-136">Les arguments de la taille et le type s’appliquent uniquement aux objets **Field** dans un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="b8cbc-136">The type and Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="b8cbc-137">Ces arguments sont ignorés lorsqu'un objet **Field** est associé à un objet **Index** ou **Relation**.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="b8cbc-138">Si le nom fait référence à un objet qui est déjà membre de la collection, une erreur d’exécution se produit lorsque vous utilisez la méthode **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="b8cbc-138">If Name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="b8cbc-p106">Pour supprimer un objet **Field** d'une collection **Fields**, utilisez la méthode **[Delete](fields-delete-method-dao.md)** dans la collection. Vous ne pouvez pas supprimer un objet **Field** dans la collection **Fields** d'un objet **TableDef** une fois que vous avez créé un index qui renvoie à ce champ.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-p106">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="b8cbc-141">**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="b8cbc-141">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="b8cbc-142">UtterAccess est un forum d’aide et wiki de Microsoft Access réputé.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-142">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="b8cbc-143">Ajout d'un champ lien hypertexte à une table existante avec DAO</span><span class="sxs-lookup"><span data-stu-id="b8cbc-143">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="b8cbc-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="b8cbc-144">Example</span></span>

<span data-ttu-id="b8cbc-p108">L'exemple suivant montre comment créer un champ calculé. La méthode CreateField crée un champ nommé **FullName**. La propriété Expression est ensuite définie sur l'expression qui calcule la valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="b8cbc-p108">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="b8cbc-148">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="b8cbc-148">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

