---
title: 'Chapitre 8 : Présentation des curseurs et des verrous'
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f2ddfab5272436b4e6ab070de30329f9c21ea4ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553213"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a>Chapitre 8 : Présentation des curseurs et des verrous

**S’applique à** : Access 2013, Office 2013

Il est important de comprendre le fonctionnement des curseurs pour sélectionner le type de curseur le plus efficace et le mieux adapté aux impératifs d'accès aux données d'une application. Une configuration du curseur inappropriée peut rendre l'accès aux données lent et laborieux.

De nombreuses fonctionnalités de l'objet **Recordset** ADO sont déterminées par le type et l'emplacement du curseur mais aussi par le type de verrou.

Ce chapitre présente les rubriques suivantes :

- [Qu’est-ce qu’un curseur ?](what-is-a-cursor.md)
- [Importance de l’emplacement du curseur](the-significance-of-cursor-location.md)
- [Service de curseur Microsoft pour OLE DB](the-microsoft-cursor-service-for-ole-db.md)
- [Utilisation de CacheSize ](using-cachesize.md)
- [Caractéristiques du curseur et du verrou](cursor-and-lock-characteristics.md)
- [Types de curseurs (ADO)](types-of-cursors.md)
- [Qu’est-ce qu’un verrou ? (ADO)](what-is-a-lock.md)

