---
title: Workspaces Collection (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37fd4ce04dbd35fccb2356b8088450d07af203d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470297"
---
# <a name="workspaces-collection-dao"></a>Workspaces Collection (DAO)


**S’applique à**: Access 2013 | Office 2013

Une collection **Workspaces** contient tous les objets **Workspace** actifs et non masqués de l'objet **DBEngine**. (Les objets **Workspace** masqués ne sont ni ajoutés à la collection ni référencés par la variable à laquelle ils sont affectés.)

## <a name="remarks"></a>Remarques

L'objet **Workspace** permet de gérer la session active ou de démarrer une session supplémentaire.

Lorsque vous consultez ou utilisez un objet **Workspace** , vous créez automatiquement l’espace de travail par défaut, DBEngine.Workspaces(0). Les paramètres des propriétés **Name** et **UserName** de l’espace de travail par défaut sont «\#espace de travail par défaut\#» et « Admin », respectivement. Si la sécurité est activée, le paramètre de propriété **UserName** correspond au nom de l'utilisateur connecté.

Vous pouvez créer de nouveaux objets **Workspace** à l'aide de la méthode **[CreateWorkspace](dbengine-createworkspace-method-dao.md)**. Une fois le nouvel objet **Workspace** créé, vous devez l'ajouter à la collection **Workspaces** si vous devez vous y référer à partir de la collection. **Workspaces** Toutefois, vous pouvez utiliser un objet **Workspace** nouvellement créé sans l'ajouter à la collection **Workspaces**.

Pour faire référence à un objet **Workspace** d'une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des syntaxes suivantes :

**DBEngine**. **Espaces de travail** (0)

**DBEngine**. **Espaces de travail** (« nom »)

**DBEngine**. **Espaces de travail** \! \[nom\]


> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.



## <a name="example"></a>Exemple

Cet exemple crée un nouvel objet Microsoft Access et l'ajoute aux collections **Workspaces**. Il énumère ensuite les collections **Workspaces** et la collection **Properties** de chaque objet **Workspace**.

```vb 
Sub WorkspaceX() 
 
 Dim wrkNewAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 ' Create a new Microsoft Access workspace. 
 Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
 "admin", "", dbUseJet) 
 Workspaces.Append wrkNewAcc 
 
 ' Enumerate the Workspaces collection. 
 For Each wrkLoop In Workspaces 
 With wrkLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of the new 
 ' Workspace object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 Next wrkLoop 
 
 wrkNewAcc.Close 
End Sub 
```

<br/>

Cet exemple utilise la méthode **CreateWorkspace** pour créer un espace de travail Microsoft Access. Il répertorie ensuite les propriétés de l'espace de travail.

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
 Debug.Print " " & wrkLoop.Name 
 Next wrkLoop 
 
 With wrkAcc 
 ' Enumerate Properties collection of Microsoft Access 
 ' workspace. 
 Debug.Print _ 
 "Properties of unnamed Microsoft Access workspace" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 
 wrkAcc.Close 
 
End Sub 
 
```

