---
title: Fonctionnalités requises pour les fournisseurs de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404441"
---
# <a name="required-functionality-for-transport-providers"></a>Fonctionnalités requises pour les fournisseurs de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque fournisseur de transport MAPI doit :
  
- Suivez les instructions générales pour travailler avec MAPI et d’autres fournisseurs de services. Pour plus d’informations, voir [Développement d’applications MAPI](mapi-application-development.md) et Fournisseurs [de services MAPI.](mapi-service-providers.md)
    
- Exposer la DLL de son fournisseur de transport à MAPI avec sa fonction d’initialisation [XPProviderInit.](xpproviderinit.md) 
    
- Exposez à MAPI son implémentation des interfaces [IXPProvider : IUnknown](ixpprovideriunknown.md) et [IXPLogon : IUnknown.](ixplogoniunknown.md) 
    
- Exposer à MAPI et aux applications clientes son implémentation de l’interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Pour plus d’informations sur l’implémentation **d’IMAPIStatus,** voir [Status Object Implementation](status-object-implementation.md). 
    
- Implémenter une boîte de dialogue feuille de propriétés pour la configuration. Pour plus d’informations sur l’implémentation des feuilles de propriétés, voir [Implémentation de la feuille de propriétés.](property-sheet-implementation.md)
    

