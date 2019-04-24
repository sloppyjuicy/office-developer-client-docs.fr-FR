---
title: Interaction des composants et des fournisseurs MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332171"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interaction des composants et des fournisseurs MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services MAPI de tout type doivent respecter certaines recommandations pour fonctionner avec d'autres composants MAPI. Chaque fournisseur de services doit:
  
- Utilisez le fournisseur et les objets d'ouverture de session appropriés pour l'initialisation.
    
- Renvoyer une table de répartition des points d'entrée de fournisseur vers le système de messagerie lors de l'initialisation.
    
- Enregistrez une ligne de table d'État MAPI pour chaque ressource appartenant au fournisseur et appelez la méthode [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) à des moments appropriés. 
    
- Utilisez la méthode [IMAPISupport:: NewUID](imapisupport-newuid.md) pour obtenir des identificateurs uniques valides (UID). 
    
- Prendre en charge les interfaces MAPI communes sur les objets qu'elle renvoie.
    
- Utilisez les fonctions d'allocation de mémoire MAPI pour allouer de la mémoire renvoyée aux applications clientes et libérer la mémoire allouée par les autres composants du sous-système MAPI.
    
- Gérer une section de profil, si nécessaire, pour stocker les informations d'identification dans le système de messagerie sous-jacent.
    
- Utilisez la méthode [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) pour enregistrer les fonctions de prétraitement des messages. 
    
- Incluez les fichiers d'en-tête corrects (y compris mapispi. h) qui définissent les constantes, les structures, les interfaces et les valeurs de retour communes.
    
- Respectez les conventions de format d'adresse pour les types d'adresse courants.
    

