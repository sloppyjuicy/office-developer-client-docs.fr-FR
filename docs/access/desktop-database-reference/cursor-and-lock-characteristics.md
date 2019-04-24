---
title: Caractéristiques du curseur et du verrou
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41a42aa3b0c49a5d871fa7b079a26c7d8076116a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295288"
---
# <a name="cursor-and-lock-characteristics"></a>Caractéristiques du curseur et du verrou

**S’applique à** : Access 2013, Office 2013

S'il est vrai que les caractéristiques d'un curseur dépendent des fonctionnalités du fournisseur, les avantages et inconvénients suivants s'appliquent généralement aux différents types de curseurs et de verrous.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de curseur ou de verrou</p></th>
<th><p>Avantages</p></th>
<th><p>Inconvénients</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Ressources requises peu importantes</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Défilement arrière impossible</p></li>
<li><p>Pas d'accès concurrentiel aux données</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p></p>
<ul>
<li><p>Défilement</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Pas d'accès concurrentiel aux données</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p></p>
<ul>
<li><p>Accès concurrentiel aux données possible mais limité</p></li>
<li><p>Défilement</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Ressources requises plus importantes</p></li>
<li><p>Non disponible dans un scénario déconnecté</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p></p>
<ul>
<li><p>Accès concurrentiel aux données élevé</p></li>
<li><p>Défilement</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Ressources requises très importantes</p></li>
<li><p>Non disponible dans un scénario déconnecté</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Ressources requises peu importantes</p></li>
<li><p>Hautement évolutif</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Mise à jour des données par le curseur impossible</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Mises à jour par lot</p></li>
<li><p>Scénarios déconnectés autorisés</p></li>
<li><p>Accès aux données par d'autres utilisateurs possible</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Données modifiables simultanément par plusieurs utilisateurs</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Modification des données par d'autres utilisateurs impossible lorsqu'elles sont verrouillées</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Accès aux données par d'autres utilisateurs impossible lorsqu'elles sont verrouillées</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Accès aux données par d'autres utilisateurs possible</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Données modifiables simultanément par plusieurs utilisateurs</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

