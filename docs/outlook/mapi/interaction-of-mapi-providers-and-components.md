---
title: Interaction des fournisseurs et composants MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434661"
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
    
- Incluez les fichiers d’en-tête appropriés (y compris mapispi.h) qui définissent des constantes, des structures, des interfaces et des valeurs de retour communes.
    
- Respecter les conventions de format d’adresse pour les types d’adresses courants.
    

