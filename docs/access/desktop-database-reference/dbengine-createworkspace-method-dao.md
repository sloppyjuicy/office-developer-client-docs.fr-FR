---
title: Méthode DBEngine.CreateWorkspace (DAO)
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
ms.openlocfilehash: df63dfb8351da910a6f735722ef33e8ddc347150
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937812"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="18656-102">Méthode DBEngine.CreateWorkspace (DAO)</span><span class="sxs-lookup"><span data-stu-id="18656-102">DBEngine.CreateWorkspace method (DAO)</span></span>


<span data-ttu-id="18656-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18656-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="18656-104">Crée un nouvel objet **[Workspace](workspace-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="18656-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="18656-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18656-105">Syntax</span></span>

<span data-ttu-id="18656-106">*expression* . CreateWorkspace (***nom***, ***nom d’utilisateur***, ***mot de passe***, ***TypeUtilisation***)</span><span class="sxs-lookup"><span data-stu-id="18656-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="18656-107">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="18656-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="18656-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18656-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18656-109">Name</span><span class="sxs-lookup"><span data-stu-id="18656-109">Name</span></span></p></th>
<th><p><span data-ttu-id="18656-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="18656-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="18656-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="18656-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="18656-112">Description</span><span class="sxs-lookup"><span data-stu-id="18656-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18656-113">Name</span><span class="sxs-lookup"><span data-stu-id="18656-113">Name</span></span></p></td>
<td><p><span data-ttu-id="18656-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="18656-114">Required</span></span></p></td>
<td><p><span data-ttu-id="18656-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="18656-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="18656-p101">Type <strong>String</strong> qui identifie par un nom unique le nouvel objet <strong>Workspace</strong>. Consultez la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour plus d’informations sur les noms d’objets <strong>Workspace</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="18656-p101">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18656-118">UserName</span><span class="sxs-lookup"><span data-stu-id="18656-118">UserName</span></span></p></td>
<td><p><span data-ttu-id="18656-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="18656-119">Required</span></span></p></td>
<td><p><span data-ttu-id="18656-120"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="18656-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="18656-p102">Type <strong>String</strong> qui identifie le propriétaire du nouvel objet <strong>Workspace</strong>. Pour plus d’informations, consultez la propriété <strong>UserName</strong>.</span><span class="sxs-lookup"><span data-stu-id="18656-p102">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object. See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18656-123">Password</span><span class="sxs-lookup"><span data-stu-id="18656-123">Password</span></span></p></td>
<td><p><span data-ttu-id="18656-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="18656-124">Required</span></span></p></td>
<td><p><span data-ttu-id="18656-125"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="18656-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="18656-126">Une <strong>chaîne</strong> contenant le mot de passe pour le nouvel objet <strong>Workspace</strong> .</span><span class="sxs-lookup"><span data-stu-id="18656-126">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="18656-127">Le mot de passe peut comporter jusqu'à 20 caractères et peut inclure n’importe quel caractère à l’exception du caractère ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="18656-127">The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>
<td><p><span data-ttu-id="18656-128"><strong>Remarque</strong>: utilisez des mots de passe forts combinant des majuscules et minuscules, nombres et des symboles.</span><span class="sxs-lookup"><span data-stu-id="18656-128"><strong>NOTE</strong>: Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="18656-129">Les mots de passe faibles ne regroupent pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="18656-129">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="18656-130">Mot de passe fort : Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="18656-130">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="18656-131">Mot de passe faible : Maison27.</span><span class="sxs-lookup"><span data-stu-id="18656-131">Weak password: House27.</span></span> <span data-ttu-id="18656-132">Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</span><span class="sxs-lookup"><span data-stu-id="18656-132">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18656-133">TypeUtilisation</span><span class="sxs-lookup"><span data-stu-id="18656-133">UseType</span></span></p></td>
<td><p><span data-ttu-id="18656-134">Facultatif</span><span class="sxs-lookup"><span data-stu-id="18656-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="18656-135"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="18656-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="18656-136">Une des valeurs de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="18656-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="18656-137"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="18656-137"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="18656-138">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="18656-138">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="18656-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="18656-139">Return value</span></span>

<span data-ttu-id="18656-140">Workspace</span><span class="sxs-lookup"><span data-stu-id="18656-140">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="18656-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="18656-141">Remarks</span></span>

<span data-ttu-id="18656-142">Dès que vous utilisez la méthode **CreateWorkspace** pour créer un nouvel objet **Workspace**, une session **Workspace** est démarrée et vous pouvez référencer l'objet **Workspace** dans votre application.</span><span class="sxs-lookup"><span data-stu-id="18656-142">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="18656-p106">Les objets **Workspace** ne sont pas permanents et vous ne pouvez pas les enregistrer sur disque. Dès que vous créez un objet **Workspace**, il est impossible de changer les paramètres de ses propriétés, à l'exception de la propriété **Name**, que vous pouvez modifier avant d'ajouter l'objet **Workspace** à la collection **[Workspaces](workspaces-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="18656-p106">**Workspace** objects aren't permanent, and you can't save them to disk. Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="18656-p107">Il n'est pas nécessaire d'ajouter le nouvel objet **Workspace** à une collection avant de pouvoir l'utiliser. Vous ajoutez un nouvel objet **Workspace** uniquement si vous devez y faire référence via la collection **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="18656-p107">You don't have to append the new **Workspace** object to a collection before you can use it. You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="18656-147">Pour supprimer un objet **Workspace** de la collection **Workspaces**, fermez toutes les bases de données et connexions ouvertes puis appelez la méthode **[Close](connection-close-method-dao.md)** sur l'objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="18656-147">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="18656-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="18656-148">Example</span></span>

<span data-ttu-id="18656-p108">Cet exemple montre comment utiliser la méthode **CreateWorkspace** pour créer un espace de travail Microsoft Access. Il donne ensuite la liste des propriétés de l'espace de travail.</span><span class="sxs-lookup"><span data-stu-id="18656-p108">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace. It then lists the properties of the workspace.</span></span>

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

