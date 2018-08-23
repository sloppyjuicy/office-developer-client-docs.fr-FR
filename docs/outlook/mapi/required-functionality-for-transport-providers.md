---
title: Fonctionnalités requises pour les fournisseurs de transports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: dc1189df1b8ad8f8e613d6813681ed3f4148b122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580494"
---
# <a name="required-functionality-for-transport-providers"></a>Fonctionnalités requises pour les fournisseurs de transports

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Chaque fournisseur de transport MAPI doit :
  
- Suivez les instructions générales pour l’utilisation de MAPI et d’autres fournisseurs de services. Pour plus d’informations, voir [Développement d’applications MAPI](mapi-application-development.md) et les [Fournisseurs de services MAPI](mapi-service-providers.md).
    
- Avoir son fournisseur de transport exposent DLL MAPI sa fonction d’initialisation de [XPProviderInit](xpproviderinit.md) . 
    
- Exposer à MAPI son implémentation de la [IXPProvider : IUnknown](ixpprovideriunknown.md) et [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces. 
    
- Exposer aux applications MAPI et client son implémentation de la [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface. Pour plus d’informations sur l’implémentation de **IMAPIStatus**, voir [Implémentation d’objet état](status-object-implementation.md). 
    
- Implémenter une boîte de dialogue de feuille de propriété de configuration. Pour plus d’informations sur l’implémentation de feuilles de propriétés, voir [Implémentation de feuille de propriétés](property-sheet-implementation.md).
    

