---
title: onError, événement (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17cbeece67ffa19666f6209a38159c9a2c6a44ea
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889944"
---
# <a name="onerror-event-rds"></a>onError, événement (RDS)


**S’applique à**: Access 2013, Office 2013

L'événement **onError** est appelé chaque fois qu'une erreur se produit pendant une opération.

## <a name="syntax"></a>Syntaxe

onError*SCode*, *Description*, *Source*, *CancelDisplay*

## <a name="parameters"></a>Paramètres

  - *SCode*

  - Entier indiquant le code d'état de l'erreur.

  - *Description*

  - Valeur de type **String** reprenant une description de l'erreur.

  - *Source*

  - Valeur de type **String** indiquant la requête ou la commande à l'origine de l'erreur.

  - *CancelDisplay*

  - Valeur de type **Boolean**. Si la valeur est **True**, l'erreur n'est pas affichée dans une boîte de dialogue.

