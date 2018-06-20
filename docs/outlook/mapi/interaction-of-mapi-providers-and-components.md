---
title: Interaction des composants et fournisseurs MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cb0f8d5077b4851a50ceb8523943ae760a8ee5ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784344"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interaction des composants et fournisseurs MAPI

  
  
**S’applique à**: Outlook 
  
Fournisseurs de services MAPI de n’importe quel type doivent respecter certaines règles pour travailler avec d’autres composants MAPI. Chaque fournisseur de services doit :
  
- Utiliser les objets de fournisseur et de connexion appropriés pour l’initialisation.
    
- Renvoie un tableau de répartition des points d’entrée fournisseur au système de messagerie lors de l’initialisation.
    
- Enregistrer une ligne de tableau état MAPI pour chaque ressource détenu par le fournisseur et appelez la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) à des moments appropriés. 
    
- Utilisez la méthode [IMAPISupport::NewUID](imapisupport-newuid.md) pour obtenir les identificateurs uniques (UID) valides. 
    
- Prend en charge les interfaces MAPI courantes sur les objets qu’elle retourne.
    
- Utilisez les fonctions d’allocation de mémoire MAPI d’allocation de mémoire renvoyé vers les applications clientes et libérer de la mémoire allouée par d’autres parties du sous-système MAPI.
    
- Mettre à jour une section de profil, si nécessaire, pour stocker les informations d’identification pour le système de messagerie sous-jacent.
    
- Utilisez la méthode [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) pour inscrire les fonctions de prétraitement. 
    
- Inclure les fichiers d’en-tête appropriés (y compris les mapispi.h) qui définissent les constantes communes, des structures, des interfaces et valeurs de retour.
    
- Respecter les conventions de format d’adresse pour les types d’adresse.
    

