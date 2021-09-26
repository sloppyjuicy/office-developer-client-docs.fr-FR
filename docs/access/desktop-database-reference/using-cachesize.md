---
title: Utilisation de CacheSize (référence de base de données de bureau Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 562ccc380c69ba1974405e5d7e4f64a1583f1a4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631642"
---
# <a name="using-cachesize"></a>Utilisation de CacheSize

**S’applique à** : Access 2013, Office 2013

Utilisez la propriété **CacheSize** pour contrôler le nombre d'enregistrements à récupérer simultanément à partir du fournisseur pour les insérer dans la mémoire locale. Par exemple, si **CacheSize** a pour valeur 10, après la première ouverture de l'objet **Recordset**, le fournisseur extrait les dix premiers enregistrements pour les insérer dans la mémoire locale. À mesure que vous parcourez l'objet **Recordset**, le fournisseur retourne les données du tampon de mémoire local. Dès que vous avez dépassé le dernier enregistrement du cache, le fournisseur récupère les dix enregistrements suivants de la source de données pour les insérer dans le cache.

> [!NOTE]
> [!REMARQUE] **CacheSize** dépend de la propriété **Maximum Open Rows** spécifique au fournisseur (dans la collection **Properties** de l'objet **Recordset** ). Vous ne pouvez pas attribuer à **CacheSize** une valeur supérieure à celle de **Maximum Open Rows**. Pour modifier le nombre de lignes que le fournisseur peut ouvrir, définissez la valeur de **Maximum Open Rows**.

La valeur de **CacheSize** peut être modifiée pendant la durée de vie de l'objet **Recordset** mais sa modification affecte uniquement le nombre d'enregistrements dans le cache après des extractions successives de la source des données. La modification de la seule valeur de la propriété ne suffira pas à modifier le contenu actuel du cache.

Si le nombre d'enregistrements à récupérer est inférieur à la valeur de **CacheSize** spécifiée, le fournisseur retourne les enregistrements restants sans qu'aucune erreur ne se produise.

L'affectation de la valeur zéro à **CacheSize** est interdite et se traduit par une erreur.

Les enregistrements extraits du cache ne reflètent pas les modifications apportées simultanément par d'autres utilisateurs aux données source. Pour forcer une mise à jour de toutes les données mises en cache, utilisez la méthode [Resync ](resync-method-ado.md).

Si  **CacheSize** a une valeur supérieure à 1, les méthodes de navigation ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext et MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) risquent d’accéder à un enregistrement supprimé si la suppression a lieu après la récupération des enregistrements. Après l’extraction initiale, les suppressions suivantes ne sont pas répercutées dans votre cache de données tant que vous n’avez pas tenté d’accéder à une valeur de données d’une ligne supprimée. Toutefois, ce problème est résolu si vous affectez la valeur 1 à **CacheSize** car les lignes supprimées ne peuvent pas être extraites.

