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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315525"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fonctionne avec les fournisseurs de services dans un service de messagerie. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objets d'administration du fournisseur  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
|Identificateur de l'interface:  <br/> |IID_IProviderAdmin  <br/> |
|Type de pointeur:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](iprovideradmin-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet d'administration du fournisseur.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Fournit l'accès à la table du fournisseur du service de messagerie, une liste des fournisseurs de services dans le service de messagerie.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Ajoute un fournisseur de services au service de messagerie.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Supprime un fournisseur de services du service de messagerie.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Ouvre une section de profil à partir du profil actuel et renvoie un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.  <br/> |
   
## <a name="remarks"></a>Remarques

Les clients peuvent obtenir un pointeur vers une interface **IProviderAdmin** en appelant la méthode [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md) ; les fournisseurs de services ont passé un pointeur **IProviderAdmin** lorsque la fonction de point d'entrée de leur service de messagerie est appelée. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

