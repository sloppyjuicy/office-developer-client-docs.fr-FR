---
title: Implémentation d'une fonction de point d'entrée de fournisseur de carnet d'adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332801"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implémentation d'une fonction de point d'entrée de fournisseur de carnet d'adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu'une application cliente appelle [MAPILogonEx](mapilogonex.md) pour commencer une session à l'aide d'un profil qui contient votre fournisseur de carnet d'adresses, MAPI charge votre fournisseur et tous les autres qui font partie du profil. MAPI apprend le nom de la fonction de point d'entrée de votre fournisseur en consultant le profil. N'oubliez pas que cette fonction n'est pas la même qu'une fonction de point d'entrée DLL; consultez la documentation de **DllMain** dans la documentation Win32. 
  
Il existe plusieurs entrées, dont certaines doivent apparaître dans le fichier de configuration MAPISVC. inf, qui sont incluses dans la section profil de chaque fournisseur de carnets d'adresses. Le tableau suivant répertorie ces entrées de section de profil et indique si le fichier MAPISVC. inf doit les inclure.
  
|**Entrée de section de profil**|**conditions requises pour MAPISVC. inf**|
|:-----|:-----|
|PR_DISPLAY_NAME = _chaîne_ <br/> |Facultatif  <br/> |
|PR_PROVIDER_DISPLAY = _chaîne_ <br/> |Obligatoire  <br/> |
|PR_PROVIDER_DLL_NAME = _nom de fichier dll_ <br/> |Obligatoire  <br/> |
|PR_RESOURCE_TYPE = _long_ <br/> |Obligatoire  <br/> |
|PR_RESOURCE_FLAGS = _masque de masques_ <br/> |Facultatif  <br/> |
   
Votre fournisseur de carnet d'adresses peut placer ces informations dans un profil directement en appelant la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) de la section de profil ou indirectement en modifiant MAPISVC. inf. Les profils sont créés à l'aide des informations appropriées dans MAPISVC. INF pour les services de messagerie ou les fournisseurs de services sélectionnés. Pour plus d'informations sur l'organisation et le contenu du complément MAPISVC. INF, consultez le [format de fichier MapiSvc. inf](file-format-of-mapisvc-inf.md).
  
Le nom de la fonction de point d'entrée DLL du fournisseur de carnet d'adresses doit être [ABProviderInit](abproviderinit.md) et doit être conforme au prototype **ABProviderInit** . Effectuez les tâches suivantes dans la fonction de point d'entrée de DLL de votre fournisseur: 
  
- Vérifiez la version de l'interface du fournisseur de services (SPI) pour vous assurer que MAPI utilise une version compatible avec la version utilisée par votre fournisseur de carnet d'adresses.
    
- Instancier un objet fournisseur de carnet d'adresses.
    
N'appelez ni **MAPIInitialize** ni **MAPIUninitialize** dans cette fonction. 
  
La fonction de point d'entrée DLL instancie un objet Provider et renvoie à l'interface MAPI un pointeur vers cet objet. 
  

