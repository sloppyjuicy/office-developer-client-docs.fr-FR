---
title: Propriété TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725972"
---
# <a name="tabledefupdatable-property-dao"></a>Propriété TableDef.Updatable (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Mise à jour

*expression* Variable qui représente un objet **TableDef** .

## <a name="remarks"></a>Remarques

La valeur de la propriété **Updatable** est toujours **True** pour un nouvel objet **TableDef** nouvellement créé et **False** pour un objet **TableDef** lié. Un nouvel objet **TableDef** peut être ajouté uniquement à une base de données pour laquelle l'utilisateur actif possède une autorisation en écriture.

