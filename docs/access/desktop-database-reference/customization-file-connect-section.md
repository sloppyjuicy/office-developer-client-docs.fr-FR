---
title: Section de connexion du fichier de personnalisation
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0760912153359a8f9a1bebd5751c05ad3ec8326f
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632986"
---
# <a name="customization-file-connect-section"></a>Section de connexion du fichier de personnalisation

**S’applique à** : Access 2013, Office 2013

Le comportement par défaut du gestionnaire est de refuser toutes les connexions. La section **connect** indique les exceptions à ce comportement. Par exemple, si toutes les sections **connect** sont absentes ou vides, par défaut, aucune connexion ne peut être établie.

La section **connect** peut contenir :

- une entrée d'accès par défaut qui spécifie les opérations de lecture et d'écriture autorisées par défaut sur cette connexion. Si aucune entrée d'accès par défaut n'existe dans la section, celle-ci sera ignorée ;

- une nouvelle chaîne de connexion qui remplace la chaîne de connexion cliente.

## <a name="syntax"></a>Syntaxe

Une entrée d'accès par défaut a la forme suivante :

`Access=accessRight`

Une entrée de chaîne de connexion de remplacement a la forme suivante :

`Connect=connectionString`

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Connect</strong></p></td>
<td><p>Chaîne littérale qui indique qu'il s'agit d'une entrée de chaîne de connexion.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>connectionString</em></strong></p></td>
<td><p>Chaîne qui remplace toute la chaîne de connexion cliente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Access</strong></p></td>
<td><p>Chaîne littérale qui indique qu'il s'agit d'une entrée d'accès.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRight</em></strong></p></td>
<td><p>Un des droits d'accès suivants :</p>
<p></p>
<ul>
<li><p><strong>NoAccess</strong>  : l'utilisateur ne peut pas accéder à la source de données.</p></li>
<li><p><strong>ReadOnly</strong>  : l'utilisateur peut lire la source de données.</p></li>
<li><p><strong>ReadWrite</strong>  : l'utilisateur peut lire la source de données ou écrire dans celle-ci.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


Si vous souhaitez autoriser une connexion (désactivant en fait le comportement du responsable par défaut), définissez l’entrée d’accès dans la section connect **par** défaut sur , puis  supprimez ou commentez toute *autre section* d’identificateur de connexion.

