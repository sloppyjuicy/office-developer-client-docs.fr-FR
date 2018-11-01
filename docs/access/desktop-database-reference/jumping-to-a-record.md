---
title: Accès à un enregistrement
TOCTitle: Jumping to a Record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c88c7c5643559dabf3304863417c526a9fd15354
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873270"
---
# <a name="jumping-to-a-record"></a>Accès à un enregistrement


**S’applique à**: Access 2013, Office 2013

La méthode [Move](move-method-ado.md) vous permet d'avancer ou de reculer d'un nombre spécifié d'enregistrements dans l'objet **Recordset**, en utilisant la syntaxe suivante :

```vb 
 
oRs.Move NumRecords, Start
```

La méthode **Move** est prise en charge sur tous les objets **Recordset**.

Si l'argument *NumRecords* est supérieur à zéro, la position de l'enregistrement actif est avancée (vers la fin du **jeu d'enregistrements**). Si l'argument *NumRecords* est inférieur à zéro, la position de l'enregistrement actif est déplacée vers l'arrière (vers le début du **jeu d'enregistrements**).

Si l'appel de la méthode **Move** déplace la position de l'enregistrement actif vers un point situé avant le premier enregistrement, ADO place automatiquement l'enregistrement actif à la position précédant le premier enregistrement dans l'objet **Recordset** (la propriété **BOF** a la valeur **True **). Si vous tentez un déplacement vers l'arrière lorsque la propriété **BOF** a déjà la valeur **True**, une erreur est générée.

Si l’appel de la méthode **Move** déplace la position de l’enregistrement actif vers un point situé après le dernier enregistrement, ADO place automatiquement l’enregistrement actif à la position suivant le dernier enregistrement dans l’objet **Recordset** (la propriété **EOF** a la valeur **True**). Si vous tentez un déplacement vers l’avant lorsque la propriété **EOF** a déjà la valeur **True**, une erreur est générée.

L'appel de la méthode **Move** à partir d'un objet **Recordset** vide génère une erreur.

Si vous passez un signet dans l’argument *Start* , le déplacement est par rapport à l’objet record à ce signet, en supposant que l’objet **Recordset** prend en charge les signets. Les signets sont définis par l'intermédiaire de la propriété [Bookmark](bookmark-property-ado.md). Si aucun signet n'est spécifié, le déplacement s'applique à l'enregistrement actif.

Si vous utilisez la propriété **CacheSize** pour cache localement des enregistrements à partir du fournisseur, en passant un argument *NbEnregistrements* qui déplace la position d’enregistrement actif en dehors du groupe actuel d’enregistrements mis en cache force ADO à récupérer un nouveau groupe d’enregistrements, à partir de l’enregistrement de destination. La propriété **CacheSize** détermine la taille du nouveau groupe extrait et l’enregistrement de destination est le premier enregistrement récupéré.

