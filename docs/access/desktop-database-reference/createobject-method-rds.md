---
title: CreateObject, méthode (RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ff2381626e8cf81aa95ee9d49f9396bd4b0316
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602719"
---
# <a name="createobject-method-rds"></a>CreateObject, méthode (RDS)


**S’applique à**: Access 2013 | Office 2013


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

  - *Object*

  - Variable objet correspondant à un objet du type spécifié dans *ProgID*.

  - *DataSpace*

  - Variable objet représentant un objet [RDS.DataSpace](dataspace-object-rds.md) utilisé pour créer une instance du nouvel objet.

  - *ProgID*

  - Valeur de type **String** contenant l'identificateur programmatique spécifiant un objet métier côté serveur qui implémente les règles métier de votre application.

  - *awebsrvr* ou *computername*

<<<<<<< Tête
  - Valeur de type **String** représentant une URL qui identifie le serveur Web IIS sur lequel une instance de l'objet métier du serveur est créée.

## <a name="remarks"></a>Notes

<a name="the-http-protocol-is-the-standard-web-protocol-https-is-a-secure-web-protocol-use-the-dcom-protocol-when-running-a-local-area-network-without-http-the-in-process-protocol-is-a-local-dynamic-link-library-dll-it-does-not-use-a-network"></a>Le *protocole HTTP* est le protocole Web standard ; *HTTPS* est un protocole Web sécurisé. Utiliser le *protocole DCOM* lors de l’exécution d’un réseau local sans protocole HTTP. Le protocole *in-process* est une bibliothèque de liens dynamiques (DLL) ; locale Il n’utilise pas un réseau.
=======
  - Une valeur de **type String** qui représente une URL qui identifie le serveur web Internet Information Services (IIS) où une instance de l’objet métier du serveur est créée.

## <a name="remarks"></a>Remarques

Le *protocole HTTP* est le protocole web standard ; *HTTPS* est un protocole web sécurisé. Utiliser le *protocole DCOM* lors de l’exécution d’un réseau local sans protocole HTTP. Le protocole *in-process* est une bibliothèque de liens dynamiques (DLL) ; locale Il n’utilise pas un réseau.
>>>>>>> master

