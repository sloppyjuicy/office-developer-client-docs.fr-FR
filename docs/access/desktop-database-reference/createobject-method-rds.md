---
title: CreateObject, méthode (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ea1f2c284b4db91df5c526950d135e277d76fb71
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627696"
---
# <a name="createobject-method-rds"></a>CreateObject, méthode (RDS)

**S’applique à** : Access 2013, Office 2013

Crée le proxy pour l'objet métier cible et retourne un pointeur vers ce proxy. Le proxy procède à l'empaquetage des données et à leur marshaling sur le stub côté serveur afin d'autoriser les communications avec l'objet métier et d'envoyer des requêtes et des données sur Internet. Pour les objets de composant in-process, aucun proxy n'est utilisé, seul un pointeur vers l'objet est fourni.

## <a name="syntax"></a>Syntaxe

RDS (Remote Data Service) prend en charge les protocoles suivants : HTTP, HTTPS (HTTP sur SSL), DCOM et in-process.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Protocole</p></th>
<th><p>Syntaxe</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>HTTP</p></td>
<td><p><em>SetobjectDataSpace</em><em></em> = . CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p><em>SetobjectDataSpace</em><em></em> = . CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p><em>SetobjectDataSpace</em><em></em> = . CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</p></td>
</tr>
<tr class="even">
<td><p>In-process</p></td>
<td><p><em>SetobjectDataSpace</em><em></em> = . CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Object* |Variable objet correspondant à un objet du type spécifié dans *ProgID*.|
|*DataSpace* |Variable objet représentant un objet [RDS.DataSpace](dataspace-object-rds.md) utilisé pour créer une instance du nouvel objet.|
|*ProgID* |Valeur de type **String** contenant l'identificateur programmatique spécifiant un objet métier côté serveur qui implémente les règles métier de votre application.|
|*awebsrvr* ou *computername* |Valeur **de type String** qui représente une URL identifiant le serveur web Internet Information Services (IIS) sur lequel une instance de l’objet métier serveur est créée.|

## <a name="remarks"></a>Remarques

Le *protocole HTTP* est le protocole web standard ; *HTTPS* est un protocole web sécurisé. Utilisez le *protocole DCOM* en cas d'exécution sur un réseau local sans protocole HTTP. Le protocole *in-process* est une bibliothèque DLL locale et n'utilise pas de réseau.

