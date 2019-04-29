---
title: Fonctionnalité requise pour les fournisseurs de transport
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
# <a name="required-functionality-for-transport-providers"></a>Fonctionnalité requise pour les fournisseurs de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Chaque fournisseur de transport MAPI doit:
  
- Suivez les instructions générales relatives à l'utilisation de MAPI et d'autres fournisseurs de services. Pour plus d'informations, consultez la rubrique [MAPI Application Development](mapi-application-development.md) and [MAPI service](mapi-service-providers.md)Providers.
    
- Sa DLL de fournisseur de transport expose à MAPI sa fonction d'initialisation [XPProviderInit](xpproviderinit.md) . 
    
- Exposer à l'interface MAPI son implémentation des interfaces [IXPProvider: IUnknown](ixpprovideriunknown.md) et [IXPLogon: IUnknown](ixplogoniunknown.md) . 
    
- Exposer aux applications MAPI et client son implémentation de l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) . Pour plus d'informations sur l'implémentation de **IMAPIStatus**, voir [Status implémentation Object](status-object-implementation.md). 
    
- Implémentez une boîte de dialogue de feuille de propriétés pour la configuration. Pour plus d'informations sur l'implémentation des feuilles de propriétés, voir implémentation de la [feuille de propriétés](property-sheet-implementation.md).
    

