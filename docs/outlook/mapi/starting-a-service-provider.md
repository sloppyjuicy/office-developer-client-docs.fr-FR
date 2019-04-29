---
title: Démarrage d'un fournisseur de services
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439554"
---
# <a name="starting-a-service-provider"></a>Démarrage d'un fournisseur de services

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
À un moment donné, une fois qu'un client a démarré une session avec MAPI, votre fournisseur de services est démarré. Les fournisseurs de transport sont démarrés lorsqu'un client effectue une demande pour ses services. Les fournisseurs de carnet d'adresses et de banque de messages sont démarrés au cours du processus d'ouverture de session du client.
  
Un client appelle [IMAPISession:: OpenAddressBook](imapisession-openaddressbook.md) pour charger chacun des fournisseurs de carnet d'adresses inclus dans le profil et [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) pour charger un fournisseur de banque de messages spécifique. Les fournisseurs de carnet d'adresses qui font partie d'un service de messagerie sont démarrés avant tous les autres fournisseurs du service. 
  
MAPI démarre chaque fournisseur de services dans le profil actif en procédant comme suit:
  
- Recherche du nom de la DLL dans le profil. Vous devez enregistrer le nom de votre DLL de fournisseur dans le fichier de configuration MAPISVC. inf pour vous assurer qu'il apparaît dans le profil. Lorsque votre fournisseur de services est ajouté à un profil, individuellement ou en tant que partie d'un service de messagerie, toutes les sections **[fournisseur de services]** de MAPISVC. inf qui s'appliquent à votre fournisseur sont copiées dans le profil. Pour plus d'informations sur la structure de MAPISVC. inf, consultez le [format de fichier MAPISVC. inf](file-format-of-mapisvc-inf.md).
    
- Appel de la fonction **LoadLibrary** de l'API Windows pour charger la dll. Étant donné que MAPI appelle **LoadLibrary** à chaque fois qu'il utilise une dll de fournisseur de services (qu'il ait déjà été chargé) ou seulement la première fois, votre fournisseur de services ne doit pas formuler de suppositions quant au nombre de fois qu'il sera chargé. Pour chaque appel à **LoadLibrary**, MAPI appelle la fonction de l'API Windows **FREELIBRARY** lorsqu'une dll de fournisseur de services n'est plus nécessaire. 
    
- Appel de la fonction de point d'entrée pour le fournisseur. MAPI appelle la fonction de point d'entrée de votre fournisseur pour lancer le processus d'ouverture de session. Les fonctions de point d'entrée garantissent que vous utilisez une version de l'interface du fournisseur de services (SPI) compatible avec la version utilisée par MAPI. Ces fonctions renvoient également des pointeurs vers des objets fournisseurs nouvellement créés. Pour plus d'informations sur la création d'une fonction de point d'entrée pour votre fournisseur, consultez la rubrique [implémentation d'une fonction de point d'entrée de fournisseur de services](implementing-a-service-provider-entry-point-function.md).
    
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

