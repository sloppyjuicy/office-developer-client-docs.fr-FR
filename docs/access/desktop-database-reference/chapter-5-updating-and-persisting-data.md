---
title: 'Chapitre 5 : Mise à jour et persistance des données'
TOCTitle: 'Chapter 5: Updating and Persisting Data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 487fd11112375fb0f5788505d049a4fc71e245ba
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861973"
---
# <a name="chapter-5-updating-and-persisting-data"></a>Chapitre 5 : Mise à jour et persistance des données


**S’applique à**: Access 2013 | Office 2013

Les chapitres précédents ont présenté la marche à suivre dans ADO pour accéder aux données d'une source de données, pour se déplacer dans les données et pour les modifier. Si l'application est évidemment conçue pour permettre aux utilisateurs de modifier ces données, il est tout aussi nécessaire qu'ils puissent enregistrer ces modifications. Pour ce faire, deux méthodes sont possibles : enregistrer les modifications de l'objet **Recordset** de façon persistante dans un fichier à l'aide de la méthode **Save** ou renvoyer ces modifications à la source de données, où elles seront stockées, avec les méthodes **Update** ou **UpdateBatch**.

Dans les chapitres précédents, vous avez appris à modifier les données dans plusieurs lignes de l'objet **Recordset**. Deux points méritent d'être soulignés quant à l'ajout, la suppression et la modification des lignes de données dans ADO.

D'une part, il faut savoir que les modifications ne sont pas directement appliquées à l'objet **Recordset**. Elles sont d'abord enregistrées dans un *tampon de copie* interne. Si vous décidez d'annuler les modifications, elles sont supprimées. Si vous décidez de les conserver, elles sont alors appliquées à l'objet **Recordset**.

La deuxième notion est que les modifications sont que soit propagés à la source de données dès que vous déclarez que le travail sur une ligne complète (autrement dit, mode *d’exécution* ), ou toutes les modifications apportées à un ensemble de lignes sont collectées jusqu'à ce que vous déclarez le travail pour l’ensemble terminé (il s’agit le mode de *traitement par lots* ). C'est la propriété **LockType** qui détermine quand ces modifications sont appliquées à la source de données sous-jacente. **adLockOptimistic** ou **adLockPessimistic** spécifie le mode de mise à jour immédiate tandis que **adLockBatchOptimistic** spécifie le mode de mise à jour par lot. La propriété **CursorLocation** peut déterminer les paramètres disponibles pour la propriété **LockType**. Par exemple, le paramètre **adLockPessimistic** n'est pas pris en charge si la propriété **CursorLocation** a la valeur **adUseClient**.

En mode de mise à jour immédiate, chaque appel de la méthode **Update** propage les modifications à la source de données. En mode de mise à jour par lot, chaque appel de la méthode **Update** ou chaque déplacement de la position de ligne active enregistre les modifications dans le tampon de copie, mais seule la méthode **UpdateBatch** propage les modifications à la source de données.

Ce chapitre présente les rubriques suivantes :

- [Updating Data (ADO)](updating-data.md)

- [Persisting Data (ADO)](persisting-data.md)