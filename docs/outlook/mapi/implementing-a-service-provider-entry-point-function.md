---
title: Implémentation d’une fonction de point d’entrée de fournisseur de services
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332990"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implémentation d’une fonction de point d’entrée de fournisseur de services

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque DLL de fournisseur de services possède une fonction de point d’entrée que MAPI appelle pour la charger. Notez que cette fonction de point d’entrée n’est pas la même que [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), la fonction de point d’entrée DLL Win32.
  
Selon le type de votre fournisseur, votre fonction de point d’entrée de fournisseur est conforme à un prototype différent. MAPI définit différents prototypes de fonction de point d’entrée pour les fournisseurs de services.
  
|**Provider**|**Prototype de fonction de point d’entrée**|
|:-----|:-----|
|Fournisseurs de magasins de messages  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Fournisseurs de transport  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Fournisseurs de carnets d’adresses  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
La plupart des fonctionnalités de ces prototypes sont identiques pour tous les types de fournisseurs de services. 
  
Les fournisseurs de carnet d’adresses, de magasin de messages et de transport effectuent les deux tâches principales suivantes dans leurs fonctions de point d’entrée :
  
1. Vérifiez la version de l’interface du fournisseur de services (SPI) pour vous assurer que MAPI utilise une version compatible avec la version que votre fournisseur de services utilise. Utilisez le  _paramètre lpulMAPIVer,_ qui contient la version SPI MAPI, et le paramètre  _lpulProviderVer,_ qui contient votre version SPI, pour effectuer la vérification. Ces paramètres sont des nombres entièrement non signés 32 bits composés de trois parties : 
    
  - Les bits 24 à 31 représentent la version principale.
    
  - Les bits 16 à 23 représentent la version mineure.
    
  - Les bits 0 à 15 représentent l’identificateur de mise à jour. Bien que le numéro de version principal change rarement, le numéro de version mineure change chaque fois que MAPI est publié et que spi a changé. L’identificateur de mise à jour est la version de build interne de Microsoft . Il est utilisé pour suivre les modifications au cours du processus de développement. MAPI définit la constante CURRENT_SPI_VERSION, documentée dans le fichier d’en-tête Mapispi.h, pour indiquer la version SPI actuelle. Échec de votre vérification avec l’erreur MAPI_E_VERSION si vous utilisez une version de SPI plus récente que la version que MAPI utilise.
    
2. Créez une instance d’un objet fournisseur. Étant donné que votre fournisseur peut être démarré et initialisé plusieurs fois, vous devez créer une nouvelle instance chaque fois que cela se produit. Les fournisseurs sont démarrés plusieurs fois lorsqu’ils apparaissent dans plusieurs profils utilisés simultanément par un ou plusieurs clients, ou lorsqu’ils apparaissent plusieurs fois dans un seul profil. Tout comme le prototype de fonction de point d’entrée diffère en fonction du type de votre fournisseur, le type d’objet fournisseur le fait également. 
    
    Si vous écrivez un fournisseur de carnet d’adresses, implémentez [IABProvider : IUnknown](iabprovideriunknown.md). Si vous écrivez un fournisseur de magasins de messages, implémentez [IMSProvider : IUnknown](imsprovideriunknown.md). Pour plus d’informations, voir [Loading Message Store Providers](loading-message-store-providers.md).
    
    Si vous écrivez un fournisseur de transport, implémentez [IXPProvider : IUnknown](ixpprovideriunknown.md). Pour plus d’informations, [voir Initialisation du fournisseur de transport.](initializing-the-transport-provider.md)
    
## <a name="see-also"></a>Voir aussi



[Démarrage d’un fournisseur de services](starting-a-service-provider.md)

