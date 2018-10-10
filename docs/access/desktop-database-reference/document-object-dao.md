---
title: Document Object (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 60fe0519bc722e688630f13acdd6701b96beff05
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470217"
---
# <a name="document-object-dao"></a>Document Object (DAO)


**S’applique à**: Access 2013 | Office 2013

Un objet **Document** inclut des informations sur une instance d'un objet. L'objet peut être une base de données, une table enregistrée, une requête ou une relation (bases de données de moteur de base de données Microsoft Access uniquement).

## <a name="remarks"></a>Remarques

Chaque objet **Container** comporte une collection **Documents** qui contient des objets **Document** qui décrivent des instances d'objets intégrés du type spécifié par l'objet **Container**. Le tableau ci-dessous répertorie le type d'objet que chaque objet **Document** décrit, le nom de son objet **Container** et le type d'informations contenues dans l'objet **Document**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Document</p></th>
<th><p>Conteneur</p></th>
<th><p>Contient des informations sur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Base de données</p></td>
<td><p>Bases de données</p></td>
<td><p>Base de données enregistrée</p></td>
</tr>
<tr class="even">
<td><p>Table ou requête</p></td>
<td><p>Tables</p></td>
<td><p>Table ou requête enregistrée</p></td>
</tr>
<tr class="odd">
<td><p>Relation</p></td>
<td><p>Relations</p></td>
<td><p>Relation enregistrée</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!REMARQUE] Ne confondez pas les objets <STRONG>Container</STRONG> répertoriés dans le tableau précédent avec les collections du même nom. L'objet <STRONG>Container</STRONG> des bases de données renvoie à tous les objets de base de données enregistrés, mais la collection <STRONG>Databases</STRONG> renvoie uniquement aux objets de base de données ouverts dans un espace de travail déterminé.</P>



Avec un objet **Document**, vous pouvez :

  - Utiliser la propriété **Name** pour renvoyer le nom qu'un utilisateur ou le moteur de base de données Microsoft Access a donné à l'objet lorsqu'il a été créé.

  - Utiliser la propriété **Container** pour renvoyer le nom de l'objet **Container** qui contient l'objet **Document**.

  - Utiliser la propriété **Owner** pour définir ou renvoyer le propriétaire de l'objet. Pour définir la propriété **Owner**, vous devez disposer de l'autorisation d'écrire pour l'objet **Document**, et vous devez définir la propriété sur le nom d'un objet **User** ou **Group** existant.

  - Utiliser les propriétés **UserName** ou **Permissions** pour définir ou renvoyer les autorisations d'accès d'un utilisateur ou d'un groupe pour l'objet. Pour définir ces propriétés, vous devez disposer de l'autorisation d'écrire pour l'objet **Document**, et vous devez définir la propriété **UserName** sur le nom d'un objet **User** ou **Group** existant.

  - Utiliser les propriétés **DateCreated** et **LastUpdated** pour renvoyer la date et l'heure auxquelles l'objet **Document** a été créé et modifié pour la dernière fois.

Dans la mesure où un objet **Document** correspond à un objet existant, vous ne pouvez pas créer d'objet **Document** ou supprimer des objets existants. Pour faire référence à un objet **Document** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**Name, utilisez l'une formes de syntaxe suivantes :

  - **Documents**(0)

  - **Documents** («*nom*»)

  - **Documents**\!\[*nom*\]

## <a name="example"></a>Exemple

Cet exemple énumère la collection **Documents** du conteneur Tables, puis la collection **Properties** du premier objet **Document** de la collection.

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

Cet exemple utilise les propriétés **Owner** et **SystemDB** pour afficher les propriétaires de différents objets **Document**.

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

