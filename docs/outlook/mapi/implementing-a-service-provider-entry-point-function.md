---
title: Implémentation d’une fonction de point d’entrée de fournisseur de services
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 40bbe110c7453cf2360fc103710fbc3bcb7f1c67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572052"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implémentation d’une fonction de point d’entrée de fournisseur de services

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Chaque fournisseur de services DLL a une entrée fonction appels MAPI pour le charger de point. Sachez que cette fonction de point d’entrée n’est pas le même que [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), la fonction de point d’entrée DLL Win32.
  
Selon le type de votre fournisseur, la fonction de point d’entrée de votre fournisseur est conforme à un prototype différent. MAPI définit les prototypes de fonction de point d’entrée différents pour les fournisseurs de service.
  
|**Provider**|**Prototype de fonction du point d’entrée**|
|:-----|:-----|
|Fournisseurs de banque de messages  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Fournisseurs de transport  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Fournisseurs de carnet d’adresses  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
La plupart des fonctionnalités de ces prototypes est la même pour tous les types de fournisseur de service. 
  
Carnet d’adresses, banque de messages et les fournisseurs de transport effectuer deux tâches principales suivantes dans leurs fonctions de point d’entrée :
  
1. Vérifier la version de l’interface de fournisseur de service (SPI) pour vous assurer que MAPI utilise une version compatible avec la version à l’aide de votre fournisseur de services. Utilisez le paramètre _lpulMAPIVer_ , qui contient la version MAPI SPI et le paramètre _lpulProviderVer_ , qui contient votre version SPI, effectuer la vérification. Ces paramètres sont des entiers non signés 32 bits composés de trois parties : 
    
  - Bits 24 à 31 représentent la version principale.
    
  - Bits 16 à 23 représentent la version secondaire.
    
  - L’identificateur de la mise à jour représentent les bits 0 à 15. Bien que le numéro de version majeur change rarement, la numéro de version mineur modifications chaque fois que MAPI est publié et le SPI a été modifiée. L’identificateur de la mise à jour est Microsoft interne build version ; Il est utilisé pour suivre les modifications apportées au cours du processus de développement. MAPI définit la constante CURRENT_SPI_VERSION documentées dans le fichier d’en-tête Mapispi.h, pour indiquer la version actuelle de SPI. Échoué à votre contrôle avec l’erreur MAPI_E_VERSION si vous utilisez une version de l’index SPI plus récente que la version à l’aide de MAPI.
    
2. Créez une instance d’un objet de fournisseur. Étant donné que votre fournisseur peut être démarré et initialisé plusieurs fois, vous devez créer une nouvelle instance chaque fois que cela se produit. Fournisseurs sont démarrés plusieurs fois lorsqu’ils s’affichent dans plusieurs profils qui sont utilisés simultanément par un ou plusieurs clients, ou lorsqu’ils s’affichent plusieurs fois dans un seul profil. Comme le prototype de la fonction de point d’entrée diffère en fonction du type de votre fournisseur, donc ne le type d’objet fournisseur. 
    
    Si vous écrivez un fournisseur de carnet d’adresses, implémentez [IABProvider : IUnknown](iabprovideriunknown.md). Si vous écrivez un fournisseur de banque de messages, implémentez [IMSProvider : IUnknown](imsprovideriunknown.md). Pour plus d’informations, voir [Chargement de fournisseurs de banque de Message](loading-message-store-providers.md).
    
    Si vous écrivez un fournisseur de transport, implémentez [IXPProvider : IUnknown](ixpprovideriunknown.md). Pour plus d’informations, voir [l’initialisation du fournisseur de Transport](initializing-the-transport-provider.md).
    
## <a name="see-also"></a>Voir aussi



[Démarrage d’un fournisseur de services](starting-a-service-provider.md)

