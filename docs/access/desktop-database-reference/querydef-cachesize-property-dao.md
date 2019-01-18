---
title: Propriété QueryDef.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701708"
---
# <a name="querydefcachesize-property-dao"></a>Propriété QueryDef.CacheSize (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie le nombre d'enregistrements extraits d'une source de données ODBC qui seront placés dans le cache local. Valeur **Long** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . CacheSize

*expression* Variable qui représente un objet **QueryDef** .

## <a name="remarks"></a>Remarques

La valeur de la propriété **CacheSize** doit être comprise entre 5 et 1 200, tout en ne dépassant pas la mémoire disponible. La valeur habituelle est égale à 100. La valeur 0 désactive la mise en cache.

Le moteur de base de données Microsoft Access demande au cache les enregistrements dans la plage du cache et extrait les enregistrements situés en dehors de cette plage à partir du serveur.

Les enregistrements extraits du cache ne répercutent pas les modifications simultanées apportées aux données sources par les autres utilisateurs.

