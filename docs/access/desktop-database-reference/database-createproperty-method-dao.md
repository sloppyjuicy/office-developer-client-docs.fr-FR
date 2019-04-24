---
title: Database. CreateProperty, méthode (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f966e041a6d2aff773f6c3849c0846ef362d1142
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294973"
---
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="b6528-102">Database. CreateProperty, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="b6528-102">Database.CreateProperty method (DAO)</span></span>

<span data-ttu-id="b6528-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6528-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6528-104">Crée un objet utilisateur **[Property](property-object-dao.md)** (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="b6528-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="b6528-105">.</span><span class="sxs-lookup"><span data-stu-id="b6528-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="b6528-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6528-106">Syntax</span></span>

<span data-ttu-id="b6528-107">*expression* . CreateProperty (***nom***, ***type***, ***valeur***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="b6528-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="b6528-108">*expression* Variable qui représente un objet **Database** .</span><span class="sxs-lookup"><span data-stu-id="b6528-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6528-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6528-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6528-110">Nom</span><span class="sxs-lookup"><span data-stu-id="b6528-110">Name</span></span></p></th>
<th><p><span data-ttu-id="b6528-111">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="b6528-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b6528-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6528-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="b6528-113">Description</span><span class="sxs-lookup"><span data-stu-id="b6528-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6528-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="b6528-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="b6528-115">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b6528-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="b6528-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b6528-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b6528-117">Valeur de type <strong>String</strong> qui nomme de façon unique le nouvel objet <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6528-117">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="b6528-118">Voir la propriété <strong>Name</strong> pour plus d'informations sur les noms <strong>Property</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="b6528-118">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6528-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="b6528-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="b6528-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b6528-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="b6528-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b6528-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b6528-122">Constante qui définit le type de données du nouvel objet <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6528-122">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="b6528-123">Pour connaître les types de données valides, reportez-vous à la propriété <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b6528-123">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6528-124"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="b6528-124"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="b6528-125">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b6528-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="b6528-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b6528-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b6528-127"><strong>Variant</strong> contenant la valeur initiale de la propriété.</span><span class="sxs-lookup"><span data-stu-id="b6528-127">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="b6528-128">Pour plus d'informations, voir la propriété <strong><a href="field-value-property-dao.md">value</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="b6528-128">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6528-129"><em>Definition</em></span><span class="sxs-lookup"><span data-stu-id="b6528-129"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="b6528-130">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b6528-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="b6528-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b6528-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b6528-132">Valeur de type <strong>Variant</strong> (sous-type <strong>Boolean</strong>) indiquant si l'objet <strong>Property</strong> est ou non un objet DDL.</span><span class="sxs-lookup"><span data-stu-id="b6528-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="b6528-133">La valeur par défaut est False.</span><span class="sxs-lookup"><span data-stu-id="b6528-133">The default is False.</span></span> <span data-ttu-id="b6528-134">Si DDL a la valeur true, les utilisateurs ne peuvent pas modifier ou supprimer cet objet <strong>Property</strong> , sauf s'ils disposent de l'autorisation dbSecWriteDef.</span><span class="sxs-lookup"><span data-stu-id="b6528-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="b6528-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b6528-135">Return value</span></span>

<span data-ttu-id="b6528-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="b6528-136">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="b6528-137">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6528-137">Remarks</span></span>

<span data-ttu-id="b6528-138">Vous pouvez créer un objet utilisateur **Property** uniquement dans la collection **[Properties](properties-collection-dao.md)** d'un objet qui est persistant.</span><span class="sxs-lookup"><span data-stu-id="b6528-138">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="b6528-p106">Si vous omettez une ou plusieurs parties facultatives lorsque vous utilisez **CreateProperty**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou réinitialiser la propriété correspondante avant d'ajouter le nouvel objet à une collection. Une fois que vous ajoutez l'objet, vous pouvez modifier certains de ses paramètres de propriété mais pas tous. Pour plus d'informations, reportez-vous aux rubriques des propriétés **Name**, **Type** et **Value**.</span><span class="sxs-lookup"><span data-stu-id="b6528-p106">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="b6528-142">Si name fait référence à un objet qui est déjà membre de la collection, une erreur d'exécution se produit lorsque vous utilisez la méthode **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="b6528-142">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="b6528-143">Pour supprimer un objet **Property** défini par l'utilisateur de la collection, utilisez la méthode **[Delete](fields-delete-method-dao.md)** sur la collection **Properties** .</span><span class="sxs-lookup"><span data-stu-id="b6528-143">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="b6528-144">Vous ne pouvez pas supprimer de propriétés intégrées.</span><span class="sxs-lookup"><span data-stu-id="b6528-144">You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="b6528-145">Si vous omettez l'argument DDL, sa valeur par défaut est false (non DDL).</span><span class="sxs-lookup"><span data-stu-id="b6528-145">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="b6528-146">Dans la mesure où la propriété DDL correspondante est exposée, vous devez supprimer et recréer l'objet **Property** pour passer de DDL à non DDL.</span><span class="sxs-lookup"><span data-stu-id="b6528-146">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="b6528-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6528-147">Example</span></span>

<span data-ttu-id="b6528-p109">Cet exemple tente de définir la valeur d'une propriété définie par l'utilisateur. Si la propriété n'existe pas, il utilise la méthode **CreateProperty** pour créer la nouvelle propriété et en définir la valeur. La procédure SetProperty est requise pour exécuter cette opération.</span><span class="sxs-lookup"><span data-stu-id="b6528-p109">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

```vb
    Sub CreatePropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Set the Archive property to True. 
       SetProperty dbsNorthwind, "Archive", True 
        
       With dbsNorthwind 
          Debug.Print "Properties of " & .Name 
           
          ' Enumerate Properties collection of the Northwind  
          ' database. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
     
          ' Delete the new property since this is a  
          ' demonstration. 
          .Properties.Delete "Archive" 
     
          .Close 
       End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
       booTemp As Boolean) 
     
       Dim prpNew As Property 
       Dim errLoop As Error 
     
       ' Attempt to set the specified property. 
       On Error GoTo Err_Property 
       dbsTemp.Properties("strName") = booTemp 
       On Error GoTo 0 
     
       Exit Sub 
     
    Err_Property: 
     
       ' Error 3270 means that the property was not found. 
       If DBEngine.Errors(0).Number = 3270 Then 
          ' Create property, set its value, and append it to the  
          ' Properties collection. 
          Set prpNew = dbsTemp.CreateProperty(strName, _ 
             dbBoolean, booTemp) 
          dbsTemp.Properties.Append prpNew 
          Resume Next 
       Else 
          ' If different error has occurred, display message. 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
          End 
       End If 
     
    End Sub
```
