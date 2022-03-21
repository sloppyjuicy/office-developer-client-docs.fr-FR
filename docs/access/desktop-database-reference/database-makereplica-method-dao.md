---
title: Database.MakeReplica, méthode (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 29ae25b5cf29b8a046eac3f8eadc5efff82addbe
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630773"
---
# <a name="databasemakereplica-method-dao"></a>Database.MakeReplica, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Crée un nouveau réplica à partir d’un autre réplica de base de données (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* MakeReplica(***PathName** _, _*_Description_*_, _*_Options_**)

*expression* Variable qui représente un objet **Database**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>PathName</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Chemin d'accès et nom de fichier du nouveau réplica. Si l'argument réplica correspond à un nom de fichier existant, une erreur se produit.</p></td>
</tr>
<tr class="even">
<td><p><em>Description</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Valeur de type <strong>String</strong> décrivant le réplica que vous créez.</p></td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> qui spécifie les caractéristiques du réplica que vous créez.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Les propriétés **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** d'un réplica nouvellement créé sont toutes affectées de la valeur **False**, ce qui signifie que les tables ne comporteront pas de données.

## <a name="example"></a>Exemple

Cette fonction s'appuie sur la méthode **MakeReplica** pour créer un réplica supplémentaire d'un réplica-maître existant. L’argument intOptions peut être une combinaison des constantes **dbRepMakeReadOnly** et **dbRepMakePartial**, ou il peut être 0. Par exemple, pour créer un réplica partiel en lecture seule, vous devez transmettre la valeur **dbRepMakeReadOnlydbRepMakePartial** +  en tant que valeur d’intOptions.

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

