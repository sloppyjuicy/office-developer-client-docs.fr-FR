---
title: Accès à un enregistrement
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bc76b4d9efffbebe99a71bb1948b2cc7e12b73f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617985"
---
# <a name="jumping-to-a-record"></a>Accès à un enregistrement


**S’applique à** : Access 2013, Office 2013

La méthode [Move](move-method-ado.md) vous permet d'avancer ou de reculer d'un nombre spécifié d'enregistrements dans l'objet **Recordset**, en utilisant la syntaxe suivante :

```vb 
 
oRs.Move NumRecords, Start
```

La méthode **Move** est prise en charge sur tous les objets **Recordset**.

Si l'argument *NumRecords* est supérieur à zéro, la position de l'enregistrement actif est avancée (vers la fin du **jeu d'enregistrements**). Si l'argument *NumRecords* est inférieur à zéro, la position de l'enregistrement actif est déplacée vers l'arrière (vers le début du **jeu d'enregistrements**).

Si l'appel de la méthode **Move** déplace la position de l'enregistrement actif vers un point situé avant le premier enregistrement, ADO place automatiquement l'enregistrement actif à la position précédant le premier enregistrement dans l'objet **Recordset** (la propriété **BOF** a la valeur **True**). Si vous tentez un déplacement vers l'arrière lorsque la propriété **BOF** a déjà la valeur **True**, une erreur est générée.

Si l’appel de la méthode **Move** déplace la position de l’enregistrement actif vers un point situé après le dernier enregistrement, ADO place automatiquement l’enregistrement actif à la position suivant le dernier enregistrement dans l’objet **Recordset** (la propriété **EOF** a la valeur **True**). Si vous tentez un déplacement vers l’avant lorsque la propriété **EOF** a déjà la valeur **True**, une erreur est générée.

L'appel de la méthode **Move** à partir d'un objet **Recordset** vide génère une erreur.

Si vous passez un signet dans l’argument *Start*, le déplacement est effectué par rapport à l’enregistrement affecté de ce signet, en supposant que l’objet **Recordset** prenne les signets en charge. Les signets sont définis par l’intermédiaire de la propriété [Bookmark](bookmark-property-ado.md). Si aucun signet n’est spécifié, le déplacement s’applique à l’enregistrement actif.

Supposons que vous utilisiez la propriété **CacheSize** pour effectuer une mise en cache locale des enregistrements du fournisseur. Si vous passez un argument *NumRecords* qui déplace la position de l'enregistrement actif hors du groupe des enregistrements actuellement en cache, ADO extrait automatiquement un nouveau groupe d'enregistrements, à partir de l'enregistrement de destination. La propriété **CacheSize** détermine la taille du nouveau groupe extrait et l'enregistrement de destination est le premier enregistrement extrait.

