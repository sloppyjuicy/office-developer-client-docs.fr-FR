---
title: 'Chapitre 5 : Mise à jour et persistance des données'
TOCTitle: 'Chapter 5: Updating and persisting data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d829a0a6984979008d33c3c68d805e82b69799aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562852"
---
# <a name="chapter-5-updating-and-persisting-data"></a>Chapitre 5 : Mise à jour et persistance des données

**S’applique à** : Access 2013, Office 2013

Les chapitres précédents ont présenté la marche à suivre dans ADO pour accéder aux données d'une source de données, pour se déplacer dans les données et pour les modifier. Si l'application est évidemment conçue pour permettre aux utilisateurs de modifier ces données, il est tout aussi nécessaire qu'ils puissent enregistrer ces modifications. Pour ce faire, deux méthodes sont possibles : enregistrer les modifications de l'objet **Recordset** de façon persistante dans un fichier à l'aide de la méthode **Save** ou renvoyer ces modifications à la source de données, où elles seront stockées, avec les méthodes **Update** ou **UpdateBatch**.

Dans les chapitres précédents, vous avez appris à modifier les données dans plusieurs lignes de l'objet **Recordset**. Deux points méritent d'être soulignés quant à l'ajout, la suppression et la modification des lignes de données dans ADO.

D'une part, il faut savoir que les modifications ne sont pas directement appliquées à l'objet **Recordset**. Elles sont d'abord enregistrées dans un *tampon de copie* interne. Si vous décidez d'annuler les modifications, elles sont supprimées. Si vous décidez de les conserver, elles sont alors appliquées à l'objet **Recordset**.

D'autre part, les modifications sont propagées à la source de données dès que vous achevez le traitement d'une ligne (mode de mise à jour *immédiate*) ou toutes les modifications apportées à un groupe de lignes sont collectées et conservées jusqu'à ce que vous acheviez le traitement de ce groupe (mode de mise à jour *par lot*). C'est la propriété **LockType** qui détermine quand ces modifications sont appliquées à la source de données sous-jacente. **adLockOptimistic** ou **adLockPessimistic** spécifie le mode de mise à jour immédiate tandis que **adLockBatchOptimistic** spécifie le mode de mise à jour par lot. La propriété **CursorLocation** peut déterminer les paramètres disponibles pour la propriété **LockType**. Par exemple, le paramètre **adLockPessimistic** n'est pas pris en charge si la propriété **CursorLocation** a la valeur **adUseClient**.

En mode de mise à jour immédiate, chaque appel de la méthode **Update** propage les modifications à la source de données. En mode de mise à jour par lot, chaque appel de la méthode **Update** ou chaque déplacement de la position de ligne active enregistre les modifications dans le tampon de copie, mais seule la méthode **UpdateBatch** propage les modifications à la source de données.

Ce chapitre présente les rubriques suivantes :

- [Updating data (ADO)](updating-data.md)
- [Persisting data (ADO)](persisting-data.md)
