---
title: CreateObject, méthode (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f622ee94fa6e37c2f618b038aea746791e58e9b8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950080"
---
# <a name="createobject-method-rds"></a>CreateObject, méthode (RDS)

**S’applique à**: Access 2013, Office 2013

Crée le proxy pour l'objet métier cible et retourne un pointeur vers ce proxy. Le proxy procède à l'empaquetage des données et à leur marshaling sur le stub côté serveur afin d'autoriser les communications avec l'objet métier et d'envoyer des requêtes et des données sur Internet. Pour les objets de composant in-process, aucun proxy n'est utilisé, seul un pointeur vers l'objet est fourni.

## <a name="syntax"></a>Syntaxe

RDS (Remote Data Service) prend en charge les protocoles suivants : HTTP, HTTPS (HTTP sur SSL), DCOM et in-process.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td><p>Définir<em>l’objet</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</p></td>
</tr>
<tr class="even">
<td><p>HTTPS</p></td>
<td><p>Définir<em>l’objet</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</p></td>
</tr>
<tr class="odd">
<td><p>DCOM</p></td>
<td><p>Définir<em>l’objet</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>nom_ordinateur</em>&quot;)</p></td>
</tr>
<tr class="even">
<td><p>In-process</p></td>
<td><p>Définir<em>l’objet</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Objet* |Variable objet correspondant à un objet du type spécifié dans *ProgID*.|
|*DataSpace* |Variable objet représentant un objet [RDS.DataSpace](dataspace-object-rds.md) utilisé pour créer une instance du nouvel objet.|
|*ProgID* |Valeur de type **String** contenant l'identificateur programmatique spécifiant un objet métier côté serveur qui implémente les règles métier de votre application.|
|*awebsrvr* ou *computername* |Une valeur de **type String** qui représente une URL qui identifie le serveur web Internet Information Services (IIS) où une instance de l’objet métier du serveur est créée.|

## <a name="remarks"></a>Remarques

Le *protocole HTTP* est le protocole web standard ; *HTTPS* est un protocole web sécurisé. Utiliser le *protocole DCOM* lors de l’exécution d’un réseau local sans protocole HTTP. Le protocole *in-process* est une bibliothèque de liens dynamiques (DLL) ; locale Il n’utilise pas un réseau.

