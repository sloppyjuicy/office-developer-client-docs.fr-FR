---
title: Implémentation d’une fonction de point d’entrée du fournisseur de carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409712"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implémentation d’une fonction de point d’entrée du fournisseur de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’une application cliente appelle [MAPILogonEx](mapilogonex.md) pour démarrer une session à l’aide d’un profil qui contient votre fournisseur de carnet d’adresses, MAPI charge votre fournisseur et tous les autres membres du profil. MAPI apprend le nom de la fonction de point d’entrée de votre fournisseur en regardant dans le profil. N’oubliez pas que cette fonction n’est pas la même qu’une fonction de point d’entrée DLL ; voir la documentation relative **à DllMain** dans la documentation Win32. 
  
Il existe plusieurs entrées, dont certaines doivent apparaître dans le fichier de configuration mapisvc.inf, qui sont incluses dans la section profil de chaque fournisseur de carnet d’adresses. Le tableau suivant répertorie ces entrées de section de profil et indique si le fichier mapisvc.inf doit les inclure.
  
|**Entrée de section de profil**|**Condition requise pour mapisvc.inf**|
|:-----|:-----|
|PR_DISPLAY_NAME= _chaîne_ <br/> |Facultatif  <br/> |
|PR_PROVIDER_DISPLAY= _chaîne_ <br/> |Obligatoire  <br/> |
|PR_PROVIDER_DLL_NAME= _nom de fichier DLL_ <br/> |Obligatoire  <br/> |
|PR_RESOURCE_TYPE= _long_ <br/> |Obligatoire  <br/> |
|PR_RESOURCE_FLAGS= masque _de bits_ <br/> |Facultatif  <br/> |
   
Votre fournisseur de carnet d’adresses peut placer ces informations dans un profil directement en appelant la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de sa section de profil ou indirectement en modifiant MAPISVC.INF. Les profils sont créés à l’aide des informations pertinentes dans MAPISVC. INF pour les fournisseurs de services ou services de messagerie sélectionnés. Pour plus d’informations sur l’organisation et le contenu de MAPISVC. INF, voir [Format de fichier de MapiSvc.inf](file-format-of-mapisvc-inf.md).
  
Le nom de la fonction de point d’entrée DLL de votre fournisseur de carnet d’adresses doit être [ABProviderInit](abproviderinit.md) et doit être conforme au prototype **ABProviderInit.** Effectuez les tâches suivantes dans la fonction de point d’entrée DLL de votre fournisseur : 
  
- Vérifiez la version de l’interface du fournisseur de services (SPI) pour vous assurer que MAPI utilise une version compatible avec la version que votre fournisseur de carnet d’adresses utilise.
    
- Ins instantiate an address book provider object.
    
N’appelez **pas MAPIInitialize** ou **MAPIUninitialize** dans cette fonction. 
  
La fonction de point d’entrée DLL ins instantie un objet fournisseur et retourne à MAPI un pointeur vers cet objet. 
  

