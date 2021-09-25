---
title: TableDef.Updatable, propriété (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ab21e5493b1c0c3c2d1ef0cf3fffb9a9d4ff965a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580747"
---
# <a name="tabledefupdatable-property-dao"></a>TableDef.Updatable, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Type de données **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* Updatable

*expression* Variable représentant un objet **TableDef**.

## <a name="remarks"></a>Remarques

La valeur de la propriété **Updatable** est toujours **True** pour un nouvel objet **TableDef** nouvellement créé et **False** pour un objet **TableDef** lié. Un nouvel objet **TableDef** peut être ajouté uniquement à une base de données pour laquelle l'utilisateur actif possède une autorisation en écriture.

