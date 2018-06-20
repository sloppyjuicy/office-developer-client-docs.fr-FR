---
title: Démarrage d’un fournisseur de services
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 99f47ee4fe990b0e77fcf868977b72d83bfdbac7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787251"
---
# <a name="starting-a-service-provider"></a>Démarrage d’un fournisseur de services

 
  
**S’applique à**: Outlook 
  
À un moment donné après qu’un client démarre une session MAPI, votre fournisseur de services est démarré. Fournisseurs de transport sont démarrés lorsqu’un client émet une demande de leurs services. Fournisseurs de magasin de messages et du carnet d’adresses sont démarrés au cours du processus d’ouverture de session du client.
  
Un client appelle [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) pour charger chacun des fournisseurs de carnet d’adresses incluses dans le profil et [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) pour charger un fournisseur de magasin de message spécifique. Fournisseurs de carnet d’adresses qui font partie d’un service de message sont démarrés avant les autres fournisseurs dans le service. 
  
MAPI démarre chaque fournisseur de services dans le profil actif en procédant comme suit :
  
- Recherche le nom de la DLL dans le profil. Vous devez enregistrer le nom de votre fournisseur de DLL dans le fichier de configuration Mapisvc.inf pour s’assurer qu’il apparaît dans le profil. Lorsque votre fournisseur de services est ajouté à un profil, individuellement ou dans le cadre d’un service de message, toutes les sections **[Service Provider]** dans Mapisvc.inf qui s’appliquent à votre fournisseur sont copiés dans le profil. Pour plus d’informations sur la structure du fichier Mapisvc.inf, voir le [Fichier de Format de fichier MapiSvc.inf](file-format-of-mapisvc-inf.md).
    
- L’appel de la fonction API Windows **LoadLibrary** pour charger la DLL. Étant donné que les appels MAPI **LoadLibrary** soit chaque fois qu’elle utilise un fournisseur de services de DLL (indépendamment de si elle a déjà été chargé) ou uniquement la première fois, votre fournisseur de services ne doit pas apporter hypothèses quant au nombre de fois qu’elle sera chargée. Pour chaque appel à **LoadLibrary**, MAPI effectue un appel à la fonction API Windows **FreeLibrary** lorsqu’un fournisseur de service que DLL n’est plus nécessaire. 
    
- Appel de la fonction de point d’entrée pour le fournisseur. MAPI appelle la fonction de votre fournisseur de point d’entrée pour lancer le processus d’ouverture de session. Fonctions de point d’entrée Assurez-vous que vous utilisez une version de l’interface de fournisseur de service (SPI) qui est compatible avec la version en cours utilisée par MAPI. Ces fonctions renvoient également des pointeurs vers des objets de fournisseur nouvellement créé. Pour plus d’informations sur la création d’une entrée de la fonction de point de votre fournisseur, voir [implémentation d’une fonction de Point de Service fournisseur de l’entrée](implementing-a-service-provider-entry-point-function.md).
    
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

