---
title: QueryDef.CacheSize, propriété (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 07ccd63bab2b7303b97063e163ad838ac2d37d44
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558064"
---
# <a name="querydefcachesize-property-dao"></a>QueryDef.CacheSize, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie le nombre d'enregistrements extraits d'une source de données ODBC qui seront placés dans le cache local. Valeur **Long** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*.* CacheSize

*expression* Variable représentant un objet **QueryDef**.

## <a name="remarks"></a>Remarques

La valeur de la propriété **CacheSize** doit être comprise entre 5 et 1 200, tout en ne dépassant pas la mémoire disponible. La valeur habituelle est égale à 100. La valeur 0 désactive la mise en cache.

Le moteur de base de données Microsoft Access demande au cache les enregistrements dans la plage du cache et extrait les enregistrements situés en dehors de cette plage à partir du serveur.

Les enregistrements extraits du cache ne répercutent pas les modifications simultanées apportées aux données sources par les autres utilisateurs.

