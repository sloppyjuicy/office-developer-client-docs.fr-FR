---
title: Copie d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: dd68bc2054136a7f587b05dc56dbeabd06de1f08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783082"
---
# <a name="copying-a-recipient"></a>Copie d’un destinataire

  
  
**S’applique à**: Outlook 
  
Pour copier un ou plusieurs destinataires d’un conteneur vers un autre ou le conteneur de même, vérifiez que le conteneur cible est modifiable. Conteneurs sont modifiables définir l’indicateur AB_MODIFIABLE dans leur propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)).
  
Pour copier une ou plusieurs entrées dans un conteneur modifiable, appelez la méthode de [IABContainer::CopyEntries](iabcontainer-copyentries.md) du conteneur de destination. Copie les entrées de carnet d’adresses peut prendre du temps, **CopyEntries** accepte quatre paramètres d’entrée : un tableau d’identificateurs d’entrée pour les entrées à copier, un handle de fenêtre, un indicateur de progression et un masque de bits d’indicateurs. 
  
L’indicateur de fenêtre poignée et la progression sont utilisés par le fournisseur de carnet d’adresses pour afficher l’état de l’opération à l’utilisateur. Si vous souhaitez afficher la progression, vous passez un handle de fenêtre de la fenêtre parent de l’indicateur de progression dans le paramètre _ulUIParam_ et ne définissez pas l’indicateur AB_NO_DIALOG dans le paramètre _ulFlags_ . Si vous disposez de votre propre implémentation d’un indicateur de progression, passer un pointeur vers l’implémentation dans le paramètre _lpProgress_ . Si ce n’est pas le cas, passez la valeur NULL. Le fournisseur de carnet d’adresses utilise l’implémentation d’indicateur de progression MAPI. 
  
Masque de bits d’indicateurs indique si vous souhaitez afficher un indicateur de progression et le doublon de vérification doivent être traités. Définir l’indicateur AB_NO_DIALOG pour supprimer un indicateur de progression. Définir l’indicateur CREATE_CHECK_DUP_LOOSE pour indiquer le fournisseur de carnet d’adresses faiblement vérifier les doublons ou les CREATE_CHECK_DUP_STRICT pour vérifier les doublons plus strict. Définir l’indicateur CREATE_REPLACE avez copiés les entrées de remplacer les entrées existantes lorsque le fournisseur détermine de doublons. 
  
Lors de la copie dans un conteneur de carnet d’adresses personnel, le fournisseur copie certaines ou toutes les propriétés de chaque entrée. Étant donné que MAPI n’établit pas la configuration requise pour les fournisseurs de l’implémentation des opérations de copie de conteneur, vous ne pouvez pas n’hypothèses sur le nombre et le type des propriétés sont copiées avec une entrée de carnet d’adresses.
  

