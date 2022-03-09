---
title: Interaction des fournisseurs et composants MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
ms.openlocfilehash: 7ed628d442c926a48c766e1627f5db8486cf14c8
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370791"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interaction des fournisseurs et composants MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services MAPI de tout type doivent suivre certaines instructions pour travailler avec d’autres composants MAPI. Chaque fournisseur de services doit :
  
- Utilisez le fournisseur et les objets d’personnalisation appropriés pour l’initialisation.
    
- Renvoyer une table de répartition des points d’entrée du fournisseur au système de messagerie lors de l’initialisation.
    
- Inscrivez une ligne de table d’état MAPI pour chaque ressource propriétaire du fournisseur et appelez la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) au moment approprié. 
    
- Utilisez la [méthode IMAPISupport::NewUID](imapisupport-newuid.md) pour obtenir des identificateurs uniques (IUD) valides. 
    
- Prise en charge des interfaces MAPI courantes sur les objets qu’elle renvoie.
    
- Utilisez les fonctions d’allocation de mémoire MAPI pour allouer la mémoire renvoyée aux applications clientes et libérer la mémoire allouée par d’autres parties du sous-système MAPI.
    
- Conservez une section de profil, si nécessaire, pour stocker les informations d’identification dans le système de messagerie sous-jacent.
    
- Utilisez la [méthode IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) pour enregistrer toutes les fonctions de prétraitment des messages. 
    
- Incluez les fichiers d’en-tête appropriés (y compris mapispi.h) qui définissent les constantes, structures, interfaces et valeurs de retour communes.
    
- Respecter les conventions de format d’adresse pour les types d’adresses courants.
    

