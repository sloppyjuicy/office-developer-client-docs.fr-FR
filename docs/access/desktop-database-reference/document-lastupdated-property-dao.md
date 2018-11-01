---
title: Document.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad5a84dcc1765cc90fdfb08adfb6610be7057401
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879647"
---
# <a name="documentlastupdated-property-dao"></a>Document.LastUpdated Property (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . LastUpdated

*expression* Variable qui représente un objet **Document** .

## <a name="remarks"></a>Remarques

**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.

