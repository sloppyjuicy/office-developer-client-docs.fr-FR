---
title: Implémentation d’une fonction de point d’entrée du fournisseur de carnet d’adresses
description: Décrit comment implémenter une fonction de point d’entrée de fournisseur de carnet d’adresses, qui instancie un objet fournisseur et retourne à MAPI un pointeur vers cet objet.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
ms.openlocfilehash: 4e3df0adf45d7d459fe7f52d7fa4d513539cf27c
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828431"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implémentation d’une fonction de point d’entrée du fournisseur de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’une application cliente appelle [MAPILogonEx](mapilogonex.md) pour commencer une session à l’aide d’un profil qui contient votre fournisseur de carnet d’adresses, MAPI charge votre fournisseur et tous les autres qui font partie du profil. MAPI apprend le nom de la fonction de point d’entrée de votre fournisseur en examinant le profil. N’oubliez pas que cette fonction n’est pas identique à une fonction de point d’entrée DLL ; consultez la documentation de **DllMain** dans la documentation Win32. 
  
Plusieurs entrées, dont certaines doivent apparaître dans le fichier de configuration mapisvc.inf, sont incluses dans la section profil de chaque fournisseur de carnet d’adresses. Le tableau suivant répertorie ces entrées de section de profil et indique si le fichier mapisvc.inf doit les inclure ou non.
  
|**Entrée de section de profil**|**condition requise pour mapisvc.inf**|
|:-----|:-----|
|PR_DISPLAY_NAME= _chaîne_ <br/> |Facultatif  <br/> |
|PR_PROVIDER_DISPLAY= _chaîne_ <br/> |Requis  <br/> |
|PR_PROVIDER_DLL_NAME= _nom de fichier DLL_ <br/> |Requis  <br/> |
|PR_RESOURCE_TYPE= _long_ <br/> |Requis  <br/> |
|PR_RESOURCE_FLAGS= _bitmask_ <br/> |Facultatif  <br/> |
   
Votre fournisseur de carnet d’adresses peut placer ces informations directement dans un profil en appelant la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de sa section de profil ou indirectement en modifiant MAPISVC.INF. Les profils sont générés à l’aide des informations pertinentes dans MAPISVC. INF pour les fournisseurs de services ou services de message sélectionnés. Pour plus d’informations sur l’organisation et le contenu de MAPISVC. INF, consultez [Format de fichier de MapiSvc.inf](file-format-of-mapisvc-inf.md).
  
Le nom de la fonction de point d’entrée DLL de votre fournisseur de carnet d’adresses doit être [ABProviderInit](abproviderinit.md) et il doit être conforme au prototype **ABProviderInit** . Effectuez les tâches suivantes dans la fonction de point d’entrée DLL de votre fournisseur : 
  
- Vérifiez la version de l’interface du fournisseur de services (SPI) pour vous assurer que MAPI utilise une version compatible avec la version utilisée par votre fournisseur de carnet d’adresses.
    
- Instanciez un objet fournisseur de carnet d’adresses.
    
N’appelez pas **MAPIInitialize** ou **MAPIUninitialize** dans cette fonction. 
  
La fonction de point d’entrée DLL instancie un objet fournisseur et retourne à MAPI un pointeur vers cet objet. 
  

