---
title: Sections du fournisseur de services MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
ms.openlocfilehash: 8e61ff1762316c5ccfce5d8fb2e3e2698bbfdb3b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379393"
---
# <a name="mapisvcinf-service-provider-sections"></a>Sections du fournisseur de services MapiSvc.inf

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Mapisvc.inf comprend une section de fournisseur de services pour chacune des **entrées** répertoriées dans l’entrée Fournisseurs de la section services de message précédente. **Les** sections du fournisseur de services sont similaires aux sections de service de messagerie, dans la sorte que les deux types de sections contiennent des entrées de ce format : 
  
**balise de propriété** = valeur de propriété 
  
Toutefois, les sections du fournisseur de services et les sections de service de messagerie diffèrent dans le fait que ces entrées de propriété sont le seul type d’entrée inclus dans les sections du fournisseur de services. Il ne peut pas y avoir de sections supplémentaires ou liées pour les fournisseurs de services ; Toutes les informations du fournisseur de services doivent être contenues dans la même section. 
  
Certaines des propriétés définies dans les sections du service de messagerie sont également définies dans les sections du fournisseur de services, car ces propriétés sont logiques pour les deux. La **propriété PR_DISPLAY_NAME** est un exemple. Les fournisseurs de services et les services de messagerie ont un nom qui est utilisé pour l’affichage dans l’interface utilisateur de configuration. Selon le fournisseur de services, ce nom peut ou non être identique. D’autres propriétés sont spécifiques aux fournisseurs de services. 
  
Les sections des fournisseurs de services classiques incluent les entrées suivantes, qui sont toutes requises :
  
 =   PR_DISPLAY_NAME _string_
  
 =   PR_PROVIDER_DISPLAY _string_
  
 =   PR_PROVIDER_DLL_NAME _nom du fichier DLL_
  
 =   PR_RESOURCE_TYPE _long_
  
 =   PR_RESOURCE_FLAGS _masque de bits_
  
L **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) est similaire à l’entrée **PR_SERVICE_DLL_NAME** ; il indique le nom de fichier de la DLL qui contient le fournisseur de services. Le code du service de messagerie peut être stocké avec l’un de ses fournisseurs de services dans le même fichier DLL ou exister en tant que DLL distincte. Notez qu’aucun suffixe n’est inclus dans l’entrée, quelle que soit la plateforme cible . MAPI s’occupe de l’ajout d’un suffixe si nécessaire. 
  
**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) représente le type de fournisseur de services ; les fournisseurs de services le définissent sur la constante prédéfinée appropriée. Les valeurs valides sont MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER et MAPI_AB_PROVIDER.
  
Une autre entrée de propriété qui s’applique à la fois aux services de messagerie et aux fournisseurs de services, l’entrée **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indique les options. Les paramètres de cette entrée de propriété peuvent varier en fonction du fournisseur de services. Par exemple, certains fournisseurs de magasins de messages peuvent définir **PR_RESOURCE_FLAGS sur STATUS_NO_DEFAULT_STORE** s’ils ne peuvent jamais fonctionner en tant que magasin de messages par défaut. 
  
Trois exemples de sections de fournisseur de services suivent. La section **[Fournisseur AB]** est la section du fournisseur de services pour le service de carnet d’adresses par défaut. Les **sections [MsgService Prov1]** et **[MsgService Prov2]** appartiennent à Mon propre service ; La première est une section de fournisseur de carnet d’adresses et la seconde est une section de fournisseur de magasins de messages. 
  
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


