---
title: Types de verrous (référence de base de données de bureau Access)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cb277d8895bf0b068417d10663d77d9ddc73cf66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621695"
---
# <a name="types-of-locks"></a>Types de verrous


**S’applique à** : Access 2013, Office 2013



## <a name="adlockbatchoptimistic"></a>adLockBatchOptimistic

Indique des mises à jour par lot optimistes. Requis pour le mode de mise à jour par lot.

Un grand nombre d'applications extraient simultanément une série de lignes puis doivent effectuer des mises à jour coordonnées (insertions, mises à jour ou suppressions) de tout le groupe de lignes. Les curseurs par lot permettent un seul accès (aller-retour) au serveur, ce qui améliore les performances de mise à jour et diminue le trafic réseau. Si vous utilisez une bibliothèque de curseurs par lot, vous pouvez créer un curseur statique, puis le déconnecter de la source de données. À ce stade, vous pouvez alors apporter les modifications appropriées aux lignes puis vous reconnecter et publier les modifications par lot dans la source de données.

## <a name="adlockoptimistic"></a>adLockOptimistic

Indique que le fournisseur utilise le verrouillage optimiste . En d'autres termes, les enregistrements ne sont verrouillés qu'en cas d'appel de la méthode **Update**. Cela dit, il est toujours possible qu'un autre utilisateur ait modifié les données entre la modification de l'enregistrement et l'appel de la méthode **Update**, ce qui engendre des conflits. Il est donc préférable d'utiliser ce type de verrou uniquement dans les cas où les risques de collision sont réduits, ou si vous estimez que ces conflits peuvent être facilement résolus.

## <a name="adlockpessimistic"></a>adLockPessimistic

Indique un verrouillage pessimiste, enregistrement par enregistrement. Le fournisseur effectue les opérations nécessaires à une modification sécurisée des enregistrements. En règle générale, les enregistrements sont verrouillés dans la source de données, immédiatement avant leur modification. Bien entendu, cela signifie que les enregistrements ne sont plus accessibles aux autres utilisateurs une fois la procédure de modification entamée, et qu'elles ne le seront qu'une fois déverrouillées, par l'appel de la méthode **Update.** Il est conseillé d'utiliser ce type de verrou dans un système dont les données ne peuvent faire l'objet de modifications concomitantes, comme un système de réservation, par exemple.

## <a name="adlockreadonly"></a>adLockReadOnly

Indique des enregistrements en lecture seule. Vous ne pouvez pas modifier les données. Un verrou en lecture seule constitue le type de verrou le plus « rapide » car il ne requiert pas de verrouillage des enregistrements par le serveur.

## <a name="adlockunspecified"></a>adLockUnspecified

Le type de verrou n'est pas spécifié.

