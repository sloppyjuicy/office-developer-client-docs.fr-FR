---
title: DBEngine.RegisterDatabase, méthode (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 8b16102cc3983a3264d9813b4553d6a626c92907
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631610"
---
# <a name="dbengineregisterdatabase-method-dao"></a>DBEngine.RegisterDatabase, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Entre les informations de connexion pour une source de données ODBC dans le Registre Windows. Le pilote ODBC a besoin des informations de connexion lorsque la source de données ODBC est ouverte au cours d’une session.

## <a name="syntax"></a>Syntaxe

*.* RegisterDatabase(***Dsn** _, _*_Driver_*_, _*_Silent_*_, _*_Attributes_**)

*expression* Variable représentant un objet **DBEngine**.

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
<td><p><em>Dsn</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>nom utilisé dans la <strong><a href="dbengine-opendatabase-method-dao.md">méthode OpenDatabase</a></strong> . Il désigne un bloc d’informations descriptives se rapportant à la source de données. Par exemple, si la source de données est une base de données distante ODBC, il peut s’agir du nom du serveur.</p></td>
</tr>
<tr class="even">
<td><p><em>Driver</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Nom du pilote ODBC. Il ne s'agit pas du fichier DLL du pilote ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><em>Silencieux</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Booléen</strong></p></td>
<td><p><strong>True</strong> si vous ne souhaitez pas afficher les boîtes de dialogue du pilote ODBC, qui invitent à saisir des informations spécifiques au pilote, ou <strong>False</strong> si vous souhaitez les afficher. Si le mode silencieux <strong>est True</strong>, les attributs doivent contenir toutes les informations spécifiques au pilote nécessaires, sinon les boîtes de dialogue s’affichent quand même.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributs</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Liste de mots clés à ajouter au registre Windows. Les mots clés se trouvent dans une chaîne délimitée par des retours chariot.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si la base de données est déjà enregistrée (les informations de connexion sont déjà entrées) dans le registre Windows lorsque vous utilisez la méthode **RegisterDatabase**, les informations de connexion sont mises à jour.

Si la méthode **RegisterDatabase** échoue pour une raison ou une autre, aucune modification n'est apportée au registre Windows, et une erreur se produit.

Pour plus d'informations sur les pilotes ODBC comme SQL Server, reportez-vous au fichier d'aide fourni avec le pilote.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **RegisterDatabase** pour enregistrer une source de données Microsoft SQL Server appelée Éditeurs dans le registre Windows.

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

