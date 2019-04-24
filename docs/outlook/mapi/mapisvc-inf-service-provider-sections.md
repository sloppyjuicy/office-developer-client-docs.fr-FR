---
title: Sections du fournisseur de services MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309540"
---
# <a name="mapisvcinf-service-provider-sections"></a>Sections du fournisseur de services MapiSvc. inf

**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPISVC. inf inclut une section du fournisseur de services pour chacune des entrées indiquées dans l'entrée **fournisseurs** de la section services de messagerie précédente. Les sections de fournisseur de **services** sont similaires aux sections de service de messagerie dans le cas où les deux types de sections contiennent des entrées au format suivant: 
  
**propriété Tag** = valeur de la propriété 
  
Toutefois, les sections du fournisseur de services et les sections de service de messagerie diffèrent en ce que ces entrées de propriété sont le seul type d'entrée inclus dans les sections du fournisseur de services. Il ne peut pas y avoir de sections supplémentaires ou liées pour les fournisseurs de services; toutes les informations du fournisseur de services doivent être contenues dans la section 1. 
  
Certaines propriétés définies dans les sections service de message sont également définies dans les sections du fournisseur de services, car ces propriétés ont un sens pour les deux. La propriété **PR_DISPLAY_NAME** est un exemple. Les services de messagerie et les fournisseurs de services ont un nom qui est utilisé pour l'affichage dans l'interface utilisateur de configuration. Selon le fournisseur de services, ce nom peut être identique ou non. D'autres propriétés sont propres aux fournisseurs de services. 
  
Les sections de fournisseur de services classiques incluent les entrées suivantes, qui sont toutes requises:
  
**** =  _Chaîne_ PR_DISPLAY_NAME
  
**** =  _Chaîne_ PR_PROVIDER_DISPLAY
  
**PR_PROVIDER_DLL_NAME** =  _nom du fichier dll_
  
**PR_RESOURCE_TYPE** =  _long_
  
**** =  _Masque_ de PR_RESOURCE_FLAGS
  
L'entrée **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) est similaire à **PR_SERVICE_DLL_NAME**; Il indique le nom de fichier de la DLL qui contient le fournisseur de services. Le code de service de messagerie peut être stocké avec un de ses fournisseurs de services dans le même fichier DLL ou exister en tant que DLL distincte. Notez qu'aucun suffixe n'est inclus dans l'entrée, quelle que soit la plateforme cible; MAPI s'occupe de l'ajout d'un suffixe si nécessaire. 
  
**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) représente le type de fournisseur de services; les fournisseurs de services la définissent sur la constante prédéfinie appropriée. Les valeurs valides sont MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER et MAPI_AB_PROVIDER.
  
Une autre entrée de propriété qui s'applique à la fois aux services de messagerie et aux fournisseurs de services, l'entrée **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indique des options. Les paramètres de cette entrée de propriété peuvent varier en fonction du fournisseur de services. Par exemple, certains fournisseurs de banques de messages peuvent définir **PR_RESOURCE_FLAGS** sur STATUS_NO_DEFAULT_STORE s'ils ne peuvent jamais fonctionner en tant que banque de messages par défaut. 
  
Trois exemples de sections de fournisseur de services suivent. La section **[AB Provider]** est la section du fournisseur de services pour le service de carnet d'adresses par défaut. Les sections **[MsgService Prov1]** et **[MsgService Prov2]** appartiennent à mon propre service; le premier est une section de fournisseur de carnet d'adresses et le second est une section de fournisseur de magasin de messages. 
  
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


