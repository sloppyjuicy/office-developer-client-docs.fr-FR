---
title: Fournisseur Microsoft OLE DB pour Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a70294e4381413fc19ce504b3547e837ed0e9a09
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633329"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a>Fournisseur Microsoft OLE DB pour Oracle

**S’applique à** : Access 2013, Office 2013

Le fournisseur Microsoft OLE DB pour Oracle permet à ADO d'accéder aux bases de données Oracle.

## <a name="connection-string-parameters"></a>Paramètres de la chaîne de connexion

Pour vous connecter à ce fournisseur, définissez l’argument *Provider* de la propriété [ConnectionString](connectionstring-property-ado.md) sur :

```vb 
 
MSDAORA 
```

La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.

Si une requête de jointure avec un keyset ou un curseur dynamique est exécutée dans une base de données Oracle, une erreur se produit. Oracle ne prend en charge qu'un curseur statique en lecture seule.

## <a name="typical-connection-string"></a>Chaîne de connexion classique

Voici une chaîne de connexion classique pour ce fournisseur :

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
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
<td><p>Spécifie le fournisseur Microsoft OLE DB pour Oracle.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>Spécifie le nom d'un serveur.</p></td>
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


## <a name="provider-specific-connection-parameters"></a>Paramètres de connexion spécifiques au fournisseur

Le fournisseur prend en charge plusieurs paramètres de connexion qui lui sont spécifiques en plus de ceux définis par ADO. Comme les propriétés de connexion ADO, ces propriétés spécifiques au fournisseur peuvent être définies via la collection [Properties](properties-collection-ado.md) d'un objet [Connection](connection-object-ado.md) ou dans **ConnectionString**.

Ces paramètres sont décrits en détail dans le guide OLE DB Programmer's Reference (en anglais). (L'[Index des propriétés dynamiques ADO](ado-dynamic-property-index.md) est un index croisé de ces noms de paramètres et des propriétés OLE DB correspondantes.)

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Paramètre</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Window Handle</strong></p></td>
<td><p>Indique le descripteur de fenêtre à utiliser pour solliciter d'autres informations.</p></td>
</tr>
<tr class="even">
<td><p><strong>Locale Identifier</strong></p></td>
<td><p>Spécifie un nombre 32 bits unique (par exemple, 1033) qui indique les préférences relatives à la langue de l'utilisateur. Ces préférences décrivent le format de la date et de l'heure, l'ordre alphabétique utilisé pour trier les éléments, le mode de comparaison des chaînes, et ainsi de suite.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OLE DB Services</strong></p></td>
<td><p>Spécifie un masque de bits qui indique les services OLE DB à activer et à désactiver.</p></td>
</tr>
<tr class="even">
<td><p><strong>Prompt</strong></p></td>
<td><p>Indique s'il faut envoyer une invite à l'utilisateur lors de l'établissement d'une connexion.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Extended Properties</strong></p></td>
<td><p>Chaîne contenant des informations de connexion étendues spécifiques au fournisseur. Utilisez cette propriété pour obtenir des informations de connexion spécifiques au fournisseur qui ne peuvent pas être décrites via le mécanisme de propriété.</p></td>
</tr>
</tbody>
</table>

