---
title: DBEngine.CreateWorkspace, méthode (DAO)
TOCTitle: CreateWorkspace Method
ms:assetid: a7d73771-9420-0448-99e6-d6c4aa78683a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821374(v=office.15)
ms:contentKeyID: 48546888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052966
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9cd84b6b5441edda2042ce0a63ae25b2cf399bd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294347"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="6d3d3-102">DBEngine.CreateWorkspace, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d3d3-102">DBEngine.CreateWorkspace method (DAO)</span></span>

<span data-ttu-id="6d3d3-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d3d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d3d3-104">Crée un nouvel objet **[Workspace](workspace-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d3d3-105">Syntax</span></span>

<span data-ttu-id="6d3d3-106">*.* CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span><span class="sxs-lookup"><span data-stu-id="6d3d3-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="6d3d3-107">*expression* Variable représentant un objet **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d3d3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d3d3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d3d3-109">Nom</span><span class="sxs-lookup"><span data-stu-id="6d3d3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6d3d3-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="6d3d3-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="6d3d3-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="6d3d3-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="6d3d3-112">Description</span><span class="sxs-lookup"><span data-stu-id="6d3d3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d3d3-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="6d3d3-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="6d3d3-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6d3d3-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6d3d3-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6d3d3-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6d3d3-116">Type <strong>String</strong> qui identifie par un nom unique le nouvel objet <strong>Workspace</strong>.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-116">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="6d3d3-117">Voir la <strong><a href="connection-name-property-dao.md">propriété Name</a></strong> pour plus d’informations sur les noms <strong>d’espaces de travail</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d3d3-118"><em>UserName</em></span><span class="sxs-lookup"><span data-stu-id="6d3d3-118"><em>UserName</em></span></span></p></td>
<td><p><span data-ttu-id="6d3d3-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6d3d3-119">Required</span></span></p></td>
<td><p><span data-ttu-id="6d3d3-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6d3d3-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6d3d3-121">Type <strong>String</strong> qui identifie le propriétaire du nouvel objet <strong>Workspace</strong>.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-121">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="6d3d3-122">Pour plus d’informations, consultez la propriété <strong>UserName</strong>.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-122">See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d3d3-123"><em>Password</em></span><span class="sxs-lookup"><span data-stu-id="6d3d3-123"><em>Password</em></span></span></p></td>
<td><p><span data-ttu-id="6d3d3-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6d3d3-124">Required</span></span></p></td>
<td><p><span data-ttu-id="6d3d3-125"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6d3d3-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6d3d3-126">Chaîne <strong>contenant</strong> le mot de passe du nouvel <strong>objet Workspace.</strong></span><span class="sxs-lookup"><span data-stu-id="6d3d3-126">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="6d3d3-127">Le mot de passe peut comporter jusqu’à 20 caractères et peut inclure n’importe quel caractère à l’exception du caractère ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6d3d3-127">The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>
<p><span data-ttu-id="6d3d3-128"><strong>REMARQUE</strong>: utilisez des mots de passe forts qui combinent des lettres majuscules et minuscules, des chiffres et des symboles.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-128"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="6d3d3-129">Les mots de passe faibles ne regroupent pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-129">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="6d3d3-130">Mot de passe fort : Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-130">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="6d3d3-131">Mot de passe faible : Maison27.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-131">Weak password: House27.</span></span> <span data-ttu-id="6d3d3-132">Utilisez un mot de passe fort facile à mémoriser afin de ne pas avoir à le noter.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-132">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d3d3-133"><em>UseType</em></span><span class="sxs-lookup"><span data-stu-id="6d3d3-133"><em>UseType</em></span></span></p></td>
<td><p><span data-ttu-id="6d3d3-134">Facultatif</span><span class="sxs-lookup"><span data-stu-id="6d3d3-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="6d3d3-135"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6d3d3-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6d3d3-136">Une des <strong><a href="workspacetypeenum-enumeration-dao.md">valeurs WorkspaceTypeEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="6d3d3-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<p><span data-ttu-id="6d3d3-137"><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-137"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="6d3d3-138">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-138">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="6d3d3-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6d3d3-139">Return value</span></span>

<span data-ttu-id="6d3d3-140">Workspace</span><span class="sxs-lookup"><span data-stu-id="6d3d3-140">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="6d3d3-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d3d3-141">Remarks</span></span>

<span data-ttu-id="6d3d3-142">Dès que vous utilisez la méthode **CreateWorkspace** pour créer un nouvel objet **Workspace**, une session **Workspace** est démarrée et vous pouvez référencer l'objet **Workspace** dans votre application.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-142">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="6d3d3-p106">Les objets **Workspace** ne sont pas permanents et vous ne pouvez pas les enregistrer sur disque. Dès que vous créez un objet **Workspace**, il est impossible de changer les paramètres de ses propriétés, à l'exception de la propriété **Name**, que vous pouvez modifier avant d'ajouter l'objet **Workspace** à la collection **[Workspaces](workspaces-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-p106">**Workspace** objects aren't permanent, and you can't save them to disk. Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="6d3d3-p107">Il n'est pas nécessaire d'ajouter le nouvel objet **Workspace** à une collection avant de pouvoir l'utiliser. Vous ajoutez un nouvel objet **Workspace** uniquement si vous devez y faire référence via la collection **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-p107">You don't have to append the new **Workspace** object to a collection before you can use it. You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="6d3d3-147">Pour supprimer un objet **Workspace** de la collection **Workspaces**, fermez toutes les bases de données et connexions ouvertes puis appelez la méthode **[Close](connection-close-method-dao.md)** sur l'objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-147">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="6d3d3-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="6d3d3-148">Example</span></span>

<span data-ttu-id="6d3d3-p108">Cet exemple montre comment utiliser la méthode **CreateWorkspace** pour créer un espace de travail Microsoft Access. Il donne ensuite la liste des propriétés de l'espace de travail.</span><span class="sxs-lookup"><span data-stu-id="6d3d3-p108">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace. It then lists the properties of the workspace.</span></span>

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
 
```

