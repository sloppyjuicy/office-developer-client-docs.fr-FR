---
title: IProviderAdmin IUnknown
description: Décrit les propriétés et l’ordre de vtable des membres pour IProviderAdmin IUnknown, qui fonctionne avec les fournisseurs de services dans un service de message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
ms.openlocfilehash: 3e2c6abb1f18b03e92f7fff4b228116e68ee26ae
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828044"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fonctionne avec les fournisseurs de services dans un service de message. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets d’administration de fournisseur  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IProviderAdmin  <br/> |
|Type de pointeur :  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[Getlasterror](iprovideradmin-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite dans l’objet d’administration du fournisseur. |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Fournit l’accès à la table du fournisseur du service de message, une liste des fournisseurs de services dans le service de message. |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Ajoute un fournisseur de services au service de message. |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Supprime un fournisseur de services du service de message. |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Ouvre une section de profil à partir du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. |
   
## <a name="remarks"></a>Remarques

Les clients peuvent obtenir un pointeur vers une interface **IProviderAdmin** en appelant la méthode [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; Les fournisseurs de services reçoivent un pointeur **IProviderAdmin** lorsque la fonction de point d’entrée de leur service de message est appelée. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

