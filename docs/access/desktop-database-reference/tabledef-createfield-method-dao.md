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
ms.openlocfilehash: 1fd66910a3630d8968f75c5a59bb535520419994
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606982"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="c4c8f-102">Méthode TableDef.CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="c4c8f-102">TableDef.CreateField Method (DAO)</span></span>

<span data-ttu-id="c4c8f-103">**S’applique à :** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4c8f-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="c4c8f-104">Crée un objet **[Field](field-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="c4c8f-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c8f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4c8f-105">Syntax</span></span>

<span data-ttu-id="c4c8f-106">*expression* . CreateField (_**nom**_, _**Type**_, _**taille**_)</span><span class="sxs-lookup"><span data-stu-id="c4c8f-106">*expression* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span></span>

<span data-ttu-id="c4c8f-107">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="c4c8f-107">*expression* A variable that represents a **TableDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c4c8f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4c8f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4c8f-109">Name</span><span class="sxs-lookup"><span data-stu-id="c4c8f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c4c8f-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="c4c8f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c4c8f-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="c4c8f-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c4c8f-112">Description</span><span class="sxs-lookup"><span data-stu-id="c4c8f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4c8f-113">Name</span><span class="sxs-lookup"><span data-stu-id="c4c8f-113">Name</span></span></p></td>
<td><p><span data-ttu-id="c4c8f-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c4c8f-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4c8f-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4c8f-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4c8f-p101">Chaîne qui identifie de manière unique le nouvel objet <strong>Field</strong>. Reportez-vous à la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour plus d'informations sur les noms valides pour l'objet <strong>Field</strong>.  </span><span class="sxs-lookup"><span data-stu-id="c4c8f-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4c8f-118">Type</span><span class="sxs-lookup"><span data-stu-id="c4c8f-118">Type</span></span></p></td>
<td><p><span data-ttu-id="c4c8f-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c4c8f-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4c8f-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4c8f-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4c8f-p102">Constante qui détermine le type de données du nouvel objet <strong>Field</strong>. Pour connaître les types de données valides, reportez-vous à la propriété <strong><a href="field-type-property-dao.md">Type</a></strong>.  </span><span class="sxs-lookup"><span data-stu-id="c4c8f-p102">A constant that determines the data type of the new <strong>Field</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4c8f-123">Size</span><span class="sxs-lookup"><span data-stu-id="c4c8f-123">Size</span></span></p></td>
<td><p><span data-ttu-id="c4c8f-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c4c8f-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4c8f-125"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="c4c8f-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4c8f-126">Integer qui indique la taille maximale, en octets, d'un objet <strong>Field</strong> qui contient du texte.</span><span class="sxs-lookup"><span data-stu-id="c4c8f-126">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text.</span></span> <span data-ttu-id="c4c8f-127">Voir la propriété <strong><a href="field-size-property-dao.md">Size</a></strong> pour les valeurs de taille valide.</span><span class="sxs-lookup"><span data-stu-id="c4c8f-127">See the <strong><a href="field-size-property-dao.md">Size</a></strong> property for valid size values.</span></span> <span data-ttu-id="c4c8f-128">Cet argument est ignoré pour les champs numériques et de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="c4c8f-128">This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c4c8f-129"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="c4c8f-129"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="c4c8f-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c4c8f-130">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="c4c8f-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c4c8f-131">Return value</span></span>
>>>>>>> <span data-ttu-id="c4c8f-132">master</span><span class="sxs-lookup"><span data-stu-id="c4c8f-132">master</span></span>

<span data-ttu-id="c4c8f-133">Champ</span><span class="sxs-lookup"><span data-stu-id="c4c8f-133">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c8f-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="c4c8f-134">Remarks</span></span>

<span data-ttu-id="c4c8f-p104">Vous pouvez utiliser la méthode **CreateField** pour créer un champ, spécifier le nom, le type de données et la taille du champ. Si vous omettez une ou plusieurs des parties facultatives lorsque vous utilisez la méthode **CreateField**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou réinitialiser la propriété correspondante avant d'ajouter le nouvel objet à la collection. Une fois que vous avez ajouté le nouvel objet, vous pouvez modifier une partie de ses paramètres de propriété, mais pas tous. Pour plus d'informations, reportez-vous aux rubriques concernant cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c4c8f-p104">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="c4c8f-139">Les arguments de la taille et le type s’appliquent uniquement aux objets **Field** dans un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="c4c8f-139">The type and Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="c4c8f-140">Ces arguments sont ignorés lorsqu'un objet **Field** est associé à un objet **Index** ou **Relation**.</span><span class="sxs-lookup"><span data-stu-id="c4c8f-140">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="c4c8f-141">Si le nom fait référence à un objet qui est déjà membre de la collection, une erreur d’exécution se produit lorsque vous utilisez la méthode **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="c4c8f-141">If Name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="c4c8f-p106">Pour supprimer un objet **Field** d'une collection **Fields**, utilisez la méthode **[Delete](fields-delete-method-dao.md)** dans la collection. Vous ne pouvez pas supprimer un objet **Field** dans la collection **Fields** d'un objet **TableDef** une fois que vous avez créé un index qui renvoie à ce champ.</span><span class="sxs-lookup"><span data-stu-id="c4c8f-p106">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="c4c8f-144">**Lien fourni par** la Communauté [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="c4c8f-144">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="c4c8f-145">UtterAccess est le premier forum d'aide et wiki de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c4c8f-145">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="c4c8f-146">Ajout d'un champ lien hypertexte à une table existante avec DAO</span><span class="sxs-lookup"><span data-stu-id="c4c8f-146">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="c4c8f-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4c8f-147">Example</span></span>

<span data-ttu-id="c4c8f-p108">L'exemple suivant montre comment créer un champ calculé. La méthode CreateField crée un champ nommé **FullName**. La propriété Expression est ensuite définie sur l'expression qui calcule la valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="c4c8f-p108">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="c4c8f-151">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="c4c8f-151">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

