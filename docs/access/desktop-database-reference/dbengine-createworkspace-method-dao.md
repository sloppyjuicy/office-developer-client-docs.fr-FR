---
title: DBEngine.CreateWorkspace Method (DAO)
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
ms.openlocfilehash: 2464426bc7178638e8ebbfc9f5b2f6d1d1b61ca2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602586"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="27caa-102">DBEngine.CreateWorkspace Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="27caa-102">DBEngine.CreateWorkspace Method (DAO)</span></span>


<span data-ttu-id="27caa-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="27caa-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="27caa-104">Crée un nouvel objet **[Workspace](workspace-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="27caa-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="27caa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27caa-105">Syntax</span></span>

<span data-ttu-id="27caa-106">*expression* . CreateWorkspace (***nom***, ***nom d’utilisateur***, ***mot de passe***, ***TypeUtilisation***)</span><span class="sxs-lookup"><span data-stu-id="27caa-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="27caa-107">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="27caa-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="27caa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27caa-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27caa-109">Name</span><span class="sxs-lookup"><span data-stu-id="27caa-109">Name</span></span></p></th>
<th><p><span data-ttu-id="27caa-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="27caa-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="27caa-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="27caa-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="27caa-112">Description</span><span class="sxs-lookup"><span data-stu-id="27caa-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27caa-113">Name</span><span class="sxs-lookup"><span data-stu-id="27caa-113">Name</span></span></p></td>
<td><p><span data-ttu-id="27caa-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="27caa-114">Required</span></span></p></td>
<td><p><span data-ttu-id="27caa-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="27caa-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="27caa-p101">Type <strong>String</strong> qui identifie par un nom unique le nouvel objet <strong>Workspace</strong>. Consultez la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour plus d’informations sur les noms d’objets <strong>Workspace</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="27caa-p101">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27caa-118">UserName</span><span class="sxs-lookup"><span data-stu-id="27caa-118">UserName</span></span></p></td>
<td><p><span data-ttu-id="27caa-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="27caa-119">Required</span></span></p></td>
<td><p><span data-ttu-id="27caa-120"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="27caa-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="27caa-p102">Type <strong>String</strong> qui identifie le propriétaire du nouvel objet <strong>Workspace</strong>. Pour plus d’informations, consultez la propriété <strong>UserName</strong>.</span><span class="sxs-lookup"><span data-stu-id="27caa-p102">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object. See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27caa-123">Password</span><span class="sxs-lookup"><span data-stu-id="27caa-123">Password</span></span></p></td>
<td><p><span data-ttu-id="27caa-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="27caa-124">Required</span></span></p></td>
<td><p><span data-ttu-id="27caa-125"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="27caa-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="27caa-126">Une <strong>chaîne</strong> contenant le mot de passe pour le nouvel objet <strong>Workspace</strong> .</span><span class="sxs-lookup"><span data-stu-id="27caa-126">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="27caa-127">Le mot de passe peut comporter jusqu'à 20 caractères et peut inclure n’importe quel caractère à l’exception du caractère ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="27caa-127">The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="27caa-p104">[!REMARQUE] Définissez des mots de passe forts qui combinent des lettres minuscules et majuscules, des nombres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</span><span class="sxs-lookup"><span data-stu-id="27caa-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27caa-133">TypeUtilisation</span><span class="sxs-lookup"><span data-stu-id="27caa-133">UseType</span></span></p></td>
<td><p><span data-ttu-id="27caa-134">Facultatif</span><span class="sxs-lookup"><span data-stu-id="27caa-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="27caa-135"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="27caa-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="27caa-136">Une des valeurs de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="27caa-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="27caa-137">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="27caa-137">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="27caa-138">Définition de l’argument type sur <STRONG>dbUseODBC</STRONG> provoquera une erreur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="27caa-138">Setting the type argument to <STRONG>dbUseODBC</STRONG> will result in a run-time error.</span></span> <span data-ttu-id="27caa-139">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="27caa-139">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="27caa-140"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="27caa-140"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="27caa-141">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27caa-141">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="27caa-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27caa-142">Return value</span></span>
>>>>>>> <span data-ttu-id="27caa-143">master</span><span class="sxs-lookup"><span data-stu-id="27caa-143">master</span></span>

<span data-ttu-id="27caa-144">Workspace</span><span class="sxs-lookup"><span data-stu-id="27caa-144">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="27caa-145">Remarques</span><span class="sxs-lookup"><span data-stu-id="27caa-145">Remarks</span></span>

<span data-ttu-id="27caa-146">Dès que vous utilisez la méthode **CreateWorkspace** pour créer un nouvel objet **Workspace**, une session **Workspace** est démarrée et vous pouvez référencer l'objet **Workspace** dans votre application.</span><span class="sxs-lookup"><span data-stu-id="27caa-146">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="27caa-p106">Les objets **Workspace** ne sont pas permanents et vous ne pouvez pas les enregistrer sur disque. Dès que vous créez un objet **Workspace**, il est impossible de changer les paramètres de ses propriétés, à l'exception de la propriété **Name**, que vous pouvez modifier avant d'ajouter l'objet **Workspace** à la collection **[Workspaces](workspaces-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="27caa-p106">**Workspace** objects aren't permanent, and you can't save them to disk. Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="27caa-p107">Il n'est pas nécessaire d'ajouter le nouvel objet **Workspace** à une collection avant de pouvoir l'utiliser. Vous ajoutez un nouvel objet **Workspace** uniquement si vous devez y faire référence via la collection **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="27caa-p107">You don't have to append the new **Workspace** object to a collection before you can use it. You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="27caa-151">Pour supprimer un objet **Workspace** de la collection **Workspaces**, fermez toutes les bases de données et connexions ouvertes puis appelez la méthode **[Close](connection-close-method-dao.md)** sur l'objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="27caa-151">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="27caa-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="27caa-152">Example</span></span>

<span data-ttu-id="27caa-p108">Cet exemple montre comment utiliser la méthode **CreateWorkspace** pour créer un espace de travail Microsoft Access. Il donne ensuite la liste des propriétés de l'espace de travail.</span><span class="sxs-lookup"><span data-stu-id="27caa-p108">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace. It then lists the properties of the workspace.</span></span>

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

