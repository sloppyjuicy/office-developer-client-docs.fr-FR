---
title: Copie d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c9030d9341ba9aea0ce186ba4205242e5e65b1fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617047"
---
# <a name="copying-a-recipient"></a>Copie d’un destinataire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour copier un ou plusieurs destinataires d’un conteneur dans un autre conteneur ou dans le même conteneur, vérifiez d’abord que le conteneur cible est modifiable. Les conteneurs modifiables définissent l’AB_MODIFIABLE dans leur propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags).](pidtagcontainerflags-canonical-property.md)
  
Pour copier une ou plusieurs entrées dans un conteneur modifiable, appelez la méthode [IABContainer::CopyEntries](iabcontainer-copyentries.md) du conteneur de destination. Étant donné que la copie d’entrées de carnet d’adresses peut prendre du temps, **CopyEntries** accepte quatre paramètres d’entrée : un tableau d’identificateurs d’entrée pour les entrées à copier, un handle de fenêtre, un indicateur de progression et un masque de bits d’indicateurs. 
  
Le handle de fenêtre et l’indicateur de progression sont utilisés par le fournisseur de carnet d’adresses pour afficher l’état de l’opération à l’utilisateur. Si vous souhaitez afficher la progression, passez un handle de fenêtre pour la fenêtre parent de l’indicateur de progression dans le paramètre _ulUIParam_ et ne définissez pas l’indicateur AB_NO_DIALOG dans le paramètre _ulFlags._ Si vous avez votre propre implémentation d’un indicateur de progression, passez un pointeur vers l’implémentation dans _le paramètre lpProgress._ Si ce n’est pas le cas, passez NULL. Le fournisseur de carnet d’adresses utilise l’implémentation de l’indicateur de progression MAPI. 
  
Le masque de bits des indicateurs indique si vous souhaitez afficher un indicateur de progression et comment la vérification des entrées en double doit être gérée. Définissez l’AB_NO_DIALOG pour supprimer un indicateur de progression. Définissez l’CREATE_CHECK_DUP_LOOSE pour indiquer au fournisseur de carnet d’adresses de vérifier les doublons ou l’indicateur CREATE_CHECK_DUP_STRICT pour une vérification plus stricte des doublons. Définissez l CREATE_REPLACE pour que les entrées copiées remplacent les entrées existantes lorsque le fournisseur détermine qu’il existe des doublons. 
  
Lors de la copie dans un conteneur de carnet d’adresses personnel, le fournisseur copie une partie ou l’ensemble des propriétés de chaque entrée. Étant donné que MAPI n’établit pas de conditions requises pour les fournisseurs implémentant des opérations de copie de conteneur, vous ne pouvez pas faire d’hypothèses sur le nombre et le type de propriétés qui sont copiées avec une entrée de carnet d’adresses.
  

