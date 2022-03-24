---
title: IProviderAdmin IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ecbc1feabe6a0f8e5495fc6a5b89d0e2a9d64f5a
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63720196"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fonctionne avec des fournisseurs de services dans un service de messagerie. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets d’administration de fournisseur  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IProviderAdmin  <br/> |
|Type de pointeur :  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet d’administration du fournisseur. |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Permet d’accéder à la table des fournisseurs du service de messagerie, liste des fournisseurs de services dans le service de messagerie. |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Ajoute un fournisseur de services au service de messagerie. |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Supprime un fournisseur de services du service de messagerie. |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Ouvre une section de profil à partir du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. |
   
## <a name="remarks"></a>Remarques

Les clients peuvent obtenir un pointeur vers une interface **IProviderAdmin** en appelant la méthode [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; Les fournisseurs de services sont transmis un pointeur **IProviderAdmin** lorsque la fonction de point d’entrée de leur service de messagerie est appelée. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

