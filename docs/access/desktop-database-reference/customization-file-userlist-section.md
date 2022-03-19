---
title: Section UserList du fichier de personnalisation
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d6060d8d4e61934dc1a51900fb737c60dbff1628
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628865"
---
# <a name="customization-file-userlist-section"></a>Section UserList du fichier de personnalisation


**S’applique à** : Access 2013, Office 2013

La section **userlist** est liée à la section **connect** avec le même paramètre *identificateur* de section.

Cette section peut contenir une entrée d’accès *utilisateur, qui* spécifie les droits d’accès pour l’utilisateur spécifié   et remplace l’entrée d’accès par défaut dans la section **de connexion correspondante**.

## <a name="syntax"></a>Syntaxe

Une entrée d'accès utilisateur a la forme suivante :

*userName***=* accessRights***

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
<td><p><em>userName</em></p></td>
<td><p><em>Nom d'utilisateur</em> de la personne utilisant cette connexion. Les noms d'utilisateurs valides sont établis à l'aide de la boîte de dialogue du <strong>Gestionnaire des services</strong> IIS.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRights</em></strong></p></td>
<td><p>Un des droits d'accès suivants :<br />
</p>
<ul>
<li><p><strong>NoAccess</strong>  : l'utilisateur ne peut pas accéder à la source de données.</p></li>
<li><p><strong>ReadOnly</strong>  : l'utilisateur peut lire la source de données.</p></li>
<li><p><strong>ReadWrite</strong>  : l'utilisateur peut lire la source de données ou écrire dans celle-ci.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

