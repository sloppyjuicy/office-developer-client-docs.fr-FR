---
title: Types de verrous (référence de base de données du bureau Access)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47b212be1922f783889f1e5be436a616909dc5c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699533"
---
# <a name="types-of-locks"></a>Types de verrous


**S’applique à**: Access 2013, Office 2013



## <a name="adlockbatchoptimistic"></a>adLockBatchOptimistic

Indique des mises à jour par lot optimistes. Requis pour le mode de mise à jour par lot.

Un grand nombre d'applications extraient simultanément une série de lignes puis doivent effectuer des mises à jour coordonnées (insertions, mises à jour ou suppressions) de tout le groupe de lignes. Les curseurs par lot permettent un seul accès (aller-retour) au serveur, ce qui améliore les performances de mise à jour et diminue le trafic réseau. Si vous utilisez une bibliothèque de curseurs par lot, vous pouvez créer un curseur statique, puis le déconnecter de la source de données. À ce stade, vous pouvez alors apporter les modifications appropriées aux lignes puis vous reconnecter et publier les modifications par lot dans la source de données.

## <a name="adlockoptimistic"></a>adLockOptimistic

Indique que le fournisseur utilise le verrouillage optimiste . En d'autres termes, les enregistrements ne sont verrouillés qu'en cas d'appel de la méthode **Update**. Cela dit, il est toujours possible qu'un autre utilisateur ait modifié les données entre la modification de l'enregistrement et l'appel de la méthode **Update**, ce qui engendre des conflits. Il est donc préférable d'utiliser ce type de verrou uniquement dans les cas où les risques de collision sont réduits, ou si vous estimez que ces conflits peuvent être facilement résolus.

## <a name="adlockpessimistic"></a>adLockPessimistic

Indique un verrouillage pessimiste, enregistrement par enregistrement. Le fournisseur effectue les opérations nécessaires à une modification sécurisée des enregistrements. En règle générale, les enregistrements sont verrouillés dans la source de données, immédiatement avant leur modification. Bien entendu, cela signifie que les enregistrements ne sont plus accessibles aux autres utilisateurs une fois la procédure de modification entamée, et qu'elles ne le seront qu'une fois déverrouillées, par l'appel de la méthode **Update.** Il est conseillé d'utiliser ce type de verrou dans un système dont les données ne peuvent faire l'objet de modifications concomitantes, comme un système de réservation, par exemple.

## <a name="adlockreadonly"></a>adLockReadOnly

Indique des enregistrements en lecture seule. Vous ne pouvez pas modifier les données. Un verrou en lecture seule constitue le type de verrou le plus « rapide » car il ne requiert pas de verrouillage des enregistrements par le serveur.

## <a name="adlockunspecified"></a>adLockUnspecified

Le type de verrou n'est pas spécifié.

