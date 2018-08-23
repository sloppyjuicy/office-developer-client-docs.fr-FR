---
title: Implémentation d’une fonction de point d’entrée de fournisseur de carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 68ba23e6ab23ff7306cd1326b73512b1c9f2a0f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579675"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implémentation d’une fonction de point d’entrée de fournisseur de carnet d’adresses

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsqu’un client application appelle [MAPILogonEx](mapilogonex.md) pour commencer une session à l’aide d’un profil qui contient votre fournisseur de carnet d’adresses, MAPI charge votre fournisseur et toutes les personnes qui font partie du profil. MAPI reçoit le nom de la fonction de point d’entrée de votre fournisseur en examinant le profil. N’oubliez pas que cette fonction est identique à une fonction de point d’entrée DLL ; consultez la documentation de **DllMain** dans la documentation de Win32. 
  
Il existe plusieurs entrées, certains d'entre eux doivent apparaître dans le fichier de configuration mapisvc.inf, qui sont incluses dans la section profil de chaque fournisseur de carnet d’adresses. Le tableau suivant répertorie les entrées de la section profil et si le fichier mapisvc.inf doit inclure.
  
|**Entrée de section de profil**|**exigence MAPISVC.inf**|
|:-----|:-----|
|PR_DISPLAY_NAME = _chaîne_ <br/> |Facultatif  <br/> |
|PR_PROVIDER_DISPLAY = _chaîne_ <br/> |Obligatoire  <br/> |
|PR_PROVIDER_DLL_NAME = _nom du fichier DLL_ <br/> |Obligatoire  <br/> |
|PR_RESOURCE_TYPE = _long_ <br/> |Obligatoire  <br/> |
|PR_RESOURCE_FLAGS = _masque de bits_ <br/> |Facultatif  <br/> |
   
Votre fournisseur de carnet d’adresses permettre placer ces informations dans un profil directement en appelant la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la section de son profil ou indirectement en modifiant le fichier MAPISVC.INF. Profils sont créées à l’aide des informations appropriées dans le fichier MAPISVC.inf. INF pour les fournisseurs de service sélectionnée ou les services de message. Pour plus d’informations sur l’organisation et le contenu du fichier MAPISVC.inf. INF, consultez le [Fichier de Format de fichier MapiSvc.inf](file-format-of-mapisvc-inf.md).
  
Le nom de la fonction de point d’entrée DLL de votre fournisseur de carnet d’adresses doit être [ABProviderInit](abproviderinit.md) et il doit être conforme au prototype **ABProviderInit** . Dans la fonction de point d’entrée DLL de votre fournisseur, effectuez les tâches suivantes : 
  
- Vérifier la version de l’interface de fournisseur de service (SPI) pour vous assurer que MAPI utilise une version compatible avec la version à l’aide de votre fournisseur de carnet d’adresses.
    
- Instancier un objet de fournisseur de carnet d’adresses.
    
N’appelez pas **l’exécuter MAPIInitialize** ou **MAPIUninitialize** dans cette fonction. 
  
La fonction de point d’entrée DLL instancie un objet de fournisseur et renvoie à MAPI un pointeur vers cet objet. 
  

