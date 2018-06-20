---
title: Sections de fournisseur de Service de MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ad6a4661025dfd8cbd39d8f58a36d94ab997ada2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784783"
---
# <a name="mapisvcinf-service-provider-sections"></a>Sections de fournisseur de Service de MapiSvc.inf

**S’applique à**: Outlook 
  
MAPISVC.inf comprend une section de fournisseur de service pour chacune des entrées répertoriées dans l’entrée de **fournisseurs** dans la section services de message précédente. Sections de fournisseur de **service** sont similaires aux sections de service de message dans la mesure où les deux types de sections contiennent des entrées dans ce format : 
  
**balise de propriété** = valeur de la propriété 
  
Toutefois, les sections de fournisseur de service et message service diffèrent dans la mesure où ces entrées de propriété sont le seul type d’entrée inclus dans les sections de fournisseur de service. Il ne peut y avoir aucune section liées ou supplémentaires pour les fournisseurs de service ; toutes les informations de fournisseur de service doivent être contenues dans la section. 
  
Certaines des propriétés définies dans les sections de service de message sont également définies dans les sections de fournisseur de service, car ces propriétés pour les deux sens. La propriété **PR_DISPLAY_NAME** est un exemple. Fournisseurs de services et de services de messagerie ont un nom qui est utilisé pour l’affichage dans l’interface utilisateur de configuration. Selon le fournisseur de services, ce nom peut ou ne peut pas être la même. Autres propriétés sont spécifiques aux fournisseurs de services. 
  
Sections de fournisseur de service par défaut sont les entrées suivantes, qui sont nécessaires :
  
**PR_DISPLAY_NAME** =  _chaîne_
  
**PR_PROVIDER_DISPLAY** =  _chaîne_
  
**PR_PROVIDER_DLL_NAME** =  _nom de fichier DLL_
  
**PR_RESOURCE_TYPE** =  _long_
  
**PR_RESOURCE_FLAGS** =  _masque de bits_
  
L’entrée **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) est similaire à **PR_SERVICE_DLL_NAME**; Il indique le nom de fichier de la DLL qui contient le fournisseur de services. Code de service de message peut être stocké avec l’un de ses fournisseurs de service dans le même fichier DLL ou exister en tant qu’une DLL distincte. Notez qu’aucun suffixe n’est incluse dans l’entrée indépendamment de la plateforme cible ; MAPI prend en charge de l’ajout d’un suffixe si nécessaire. 
  
**PR_RESOURCE_TYPE** Entrée ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) représente le type de fournisseur de services ; fournisseurs de services de lui attribuer la constante prédéfinie appropriée. Les valeurs valides sont MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER et MAPI_AB_PROVIDER.
  
Une autre entrée de propriété s’applique aux services de messagerie et de fournisseurs de services, l’entrée **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indique les options. Les paramètres d’entrée de cette propriété peuvent être différente selon le fournisseur de services. Par exemple, certains fournisseurs de banque de message peuvent définir **PR_RESOURCE_FLAGS** à STATUS_NO_DEFAULT_STORE si elles ne peuvent jamais fonctionner en tant que la banque de messages par défaut. 
  
Suivent de trois exemples de sections de fournisseur de service. La section **[Fournisseur AB]** est la section de fournisseur de service pour le service de carnet d’adresses par défaut. Les sections **[MsgService Prov1]** et **[MsgService Prov2]** appartiennent à mon Service propre ; le premier est une section de fournisseur de carnet d’adresses et le second est une section de fournisseur de magasin de message. 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


