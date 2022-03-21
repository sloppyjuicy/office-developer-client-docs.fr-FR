---
title: Fournisseur Microsoft OLE DB pour la publication Internet
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f05942403df4253b0af66607147b44f155f5ce04
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629859"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a>Fournisseur Microsoft OLE DB pour la publication Internet

**S’applique à** : Access 2013, Office 2013

Le fournisseur Microsoft OLE DB pour la publication Internet permet à ADO d'accéder aux ressources générées par Microsoft FrontPage ou Microsoft Internet Information Server. Les ressources incluent des fichiers source Web tels que des fichiers HTML ou des dossier Web Windows 2000.

## <a name="connection-string-parameters"></a>Paramètres de chaîne de connexion

Pour vous connecter à ce fournisseur, définissez l’argument *Provider* de la propriété [ConnectionString](connectionstring-property-ado.md) sur :

```vb 
 
MSDAIPP.DSO 
```

Cette valeur peut également être définie ou lue à partir de la propriété [Provider](provider-property-ado.md).

## <a name="typical-connection-string"></a>Chaîne de connexion classique

Voici une chaîne de connexion classique pour ce fournisseur :

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

\-or-

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

La chaîne est composée des mots clé suivants :

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Keyword</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Spécifie le fournisseur Microsoft OLE DB pour la publication Internet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong> -or- <strong>URL</strong></p></td>
<td><p>Spécifie l’URL d’un fichier ou d’un répertoire publié dans un dossier web.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User ID</strong></p></td>
<td><p>Spécifie le nom de l'utilisateur.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Spécifie le mot de passe de l'utilisateur.</p></td>
</tr>
</tbody>
</table>


Si vous définissez le paramètre *ResourceURL* dans la chaîne de connexion « URL= » sur une valeur non valide, le fournisseur pour la publication Internet déclenche une boîte de dialogue vous invitant à entrer une valeur valide. Ce comportement n'est pas souhaitable pour un composant de niveau intermédiaire d'une application car il interrompt l'exécution du programme jusqu'à fermeture de la boîte de dialogue et le client se fige car il n'a pas reçu de réponse du composant.

> [!NOTE]
> Si la valeur MSDAIPP.DSO est explicitement spécifiée pour le fournisseur, que ce soit au travers du mot clé *Provider* dans la chaîne de connexion ou de la propriété  **Provider** vous ne pouvez pas utiliser « URL= » dans la chaîne de connexion. Cela générerait une erreur. Vous devez simplement spécifier l’URL comme expliqué sous la rubrique [Fournisseur OLE DB pour la publication Internet](the-ole-db-provider-for-internet-publishing.md).

