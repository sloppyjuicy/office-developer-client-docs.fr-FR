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
localization_priority: Normal
ms.openlocfilehash: 9cd84b6b5441edda2042ce0a63ae25b2cf399bd2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699883"
---
# <a name="dbenginecreateworkspace-method-dao"></a>Méthode DBEngine.CreateWorkspace (DAO)

**S’applique à**: Access 2013, Office 2013

Crée un nouvel objet **[Workspace](workspace-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . CreateWorkspace (***nom***, ***nom d’utilisateur***, ***mot de passe***, ***TypeUtilisation***)

*expression* Variable qui représente un objet **DBEngine** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Type <strong>String</strong> qui identifie par un nom unique le nouvel objet <strong>Workspace</strong>. Consultez la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour plus d’informations sur les noms d’objets <strong>Workspace</strong> valides.</p></td>
</tr>
<tr class="even">
<td><p><em>UserName</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Type <strong>String</strong> qui identifie le propriétaire du nouvel objet <strong>Workspace</strong>. Pour plus d’informations, consultez la propriété <strong>UserName</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><em>Password</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Une <strong>chaîne</strong> contenant le mot de passe pour le nouvel objet <strong>Workspace</strong> . Le mot de passe peut comporter jusqu'à 20 caractères et peut inclure n’importe quel caractère à l’exception du caractère ASCII 0 (null).</p>
<p><strong>Remarque</strong>: utilisez des mots de passe forts combinant des majuscules et minuscules, nombres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</p>
</td>
</tr>
<tr class="even">
<td><p><em>TypeUtilisation</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Une des valeurs de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>
<p><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Workspace

## <a name="remarks"></a>Remarques

Dès que vous utilisez la méthode **CreateWorkspace** pour créer un nouvel objet **Workspace**, une session **Workspace** est démarrée et vous pouvez référencer l'objet **Workspace** dans votre application.

Les objets **Workspace** ne sont pas permanents et vous ne pouvez pas les enregistrer sur disque. Dès que vous créez un objet **Workspace**, il est impossible de changer les paramètres de ses propriétés, à l'exception de la propriété **Name**, que vous pouvez modifier avant d'ajouter l'objet **Workspace** à la collection **[Workspaces](workspaces-collection-dao.md)**.

Il n'est pas nécessaire d'ajouter le nouvel objet **Workspace** à une collection avant de pouvoir l'utiliser. Vous ajoutez un nouvel objet **Workspace** uniquement si vous devez y faire référence via la collection **Workspaces**.

Pour supprimer un objet **Workspace** de la collection **Workspaces**, fermez toutes les bases de données et connexions ouvertes puis appelez la méthode **[Close](connection-close-method-dao.md)** sur l'objet **Workspace**.

## <a name="example"></a>Exemple

Cet exemple montre comment utiliser la méthode **CreateWorkspace** pour créer un espace de travail Microsoft Access. Il donne ensuite la liste des propriétés de l'espace de travail.

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

