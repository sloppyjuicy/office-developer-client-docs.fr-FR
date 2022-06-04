---
title: Démarrage d’un fournisseur de services
description: Décrit le démarrage d’un fournisseur de services dans Outlook 2013 et Outlook 2016, avec des liens vers des documents de référence.
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
ms.openlocfilehash: 7cc5a5ac89e2f83363187d0244fbfbb41c81a5c7
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894500"
---
# <a name="starting-a-service-provider"></a>Démarrage d’un fournisseur de services

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
À un moment donné, après qu’un client a démarré une session avec MAPI, votre fournisseur de services est démarré. Les fournisseurs de transport sont démarrés lorsqu’un client effectue une demande pour ses services. Les fournisseurs de carnets d’adresses et de magasins de messages sont démarrés pendant le processus d’ouverture de session du client.
  
Un client appelle [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) pour charger chacun des fournisseurs de carnets d’adresses inclus dans le profil et [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) pour charger un fournisseur de magasin de messages spécifique. Les fournisseurs de carnets d’adresses qui font partie d’un service de message sont démarrés avant l’un des autres fournisseurs du service. 
  
MAPI démarre chaque fournisseur de services dans le profil actif en procédant comme suit :
  
- Localisation du nom de sa DLL dans le profil. Vous devez inscrire le nom de votre DLL de fournisseur dans le fichier de configuration Mapisvc.inf pour vous assurer qu’il apparaît dans le profil. Lorsque votre fournisseur de services est ajouté à un profil, individuellement ou dans le cadre d’un service de message, toutes les sections **[Fournisseur** de services] de Mapisvc.inf qui s’appliquent à votre fournisseur sont copiées dans le profil. Pour plus d’informations sur la structure de Mapisvc.inf, consultez [Format de fichier de MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
- Appel de la fonction **d’API Windows LoadLibrary** pour charger la DLL. Étant donné que MAPI appelle **LoadLibrary** chaque fois qu’il utilise une DLL de fournisseur de services (qu’elle ait déjà été chargée) ou seulement la première fois, votre fournisseur de services ne doit pas faire d’hypothèses sur le nombre de fois où il sera chargé. Pour chaque appel à **LoadLibrary**, MAPI effectue un appel à la fonction API Windows **FreeLibrary** lorsqu’une DLL de fournisseur de services n’est plus nécessaire. 
    
- Appel de la fonction de point d’entrée pour le fournisseur. MAPI appelle la fonction de point d’entrée de votre fournisseur pour lancer le processus d’ouverture de session. Les fonctions de point d’entrée garantissent que vous utilisez une version de l’interface du fournisseur de services (SPI) compatible avec la version utilisée par MAPI. Ces fonctions retournent également des pointeurs vers des objets de fournisseur nouvellement créés. Pour plus d’informations sur la création d’une fonction de point d’entrée pour votre fournisseur, consultez [Implémentation d’une fonction de point d’entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md).
    
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

