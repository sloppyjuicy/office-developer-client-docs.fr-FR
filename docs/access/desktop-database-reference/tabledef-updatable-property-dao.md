---
title: TableDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44f24e68b60f69304a167d2b9b5ce0b4b0e69b11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472422"
---
# <a name="tabledefupdatable-property-dao"></a>TableDef.Updatable Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Mise à jour

*expression* Variable qui représente un objet **TableDef** .

## <a name="remarks"></a>Remarques

La valeur de la propriété **Updatable** est toujours **True** pour un nouvel objet **TableDef** nouvellement créé et **False** pour un objet **TableDef** lié. Un nouvel objet **TableDef** peut être ajouté uniquement à une base de données pour laquelle l'utilisateur actif possède une autorisation en écriture.

