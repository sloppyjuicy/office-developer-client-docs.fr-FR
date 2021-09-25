---
title: Fonctionnalités requises pour les fournisseurs de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b08057ce597459988fc443f5e7495b45fdef56a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578794"
---
# <a name="required-functionality-for-transport-providers"></a>Fonctionnalités requises pour les fournisseurs de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque fournisseur de transport MAPI doit :
  
- Suivez les instructions générales pour travailler avec MAPI et d’autres fournisseurs de services. Pour plus d’informations, voir [Développement d’applications MAPI](mapi-application-development.md) et Fournisseurs [de services MAPI.](mapi-service-providers.md)
    
- Exposer la DLL de son fournisseur de transport à MAPI avec sa fonction d’initialisation [XPProviderInit.](xpproviderinit.md) 
    
- Exposez à MAPI son implémentation des interfaces [IXPProvider : IUnknown](ixpprovideriunknown.md) et [IXPLogon : IUnknown.](ixplogoniunknown.md) 
    
- Exposer à MAPI et aux applications clientes son implémentation de l’interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Pour plus d’informations sur l’implémentation **d’IMAPIStatus,** voir [Status Object Implementation](status-object-implementation.md). 
    
- Implémenter une boîte de dialogue feuille de propriétés pour la configuration. Pour plus d’informations sur l’implémentation des feuilles de propriétés, voir [Implémentation de la feuille de propriétés.](property-sheet-implementation.md)
    

