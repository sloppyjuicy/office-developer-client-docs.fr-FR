---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437531"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fonctionne avec des fournisseurs de services dans un service de messagerie. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets d’administration de fournisseur  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IProviderAdmin  <br/> |
|Type de pointeur :  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet d’administration du fournisseur.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Permet d’accéder à la table des fournisseurs du service de messagerie, liste des fournisseurs de services dans le service de messagerie.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Ajoute un fournisseur de services au service de messagerie.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Supprime un fournisseur de services du service de messagerie.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Ouvre une section de profil à partir du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.  <br/> |
   
## <a name="remarks"></a>Remarques

Les clients peuvent obtenir un pointeur vers une interface **IProviderAdmin** en appelant la méthode [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; Les fournisseurs de services sont transmis un pointeur **IProviderAdmin** lorsque la fonction de point d’entrée de leur service de messagerie est appelée. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

