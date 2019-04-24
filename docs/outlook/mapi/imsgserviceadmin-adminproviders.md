---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317422"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur qui fournit l'accès à un objet d'administration de fournisseur.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique pour le service de messagerie à administrer. 
    
 _ulFlags_
  
> dans Toujours NULL. 
    
 _lppProviderAdmin_
  
> remarquer Pointeur vers un pointeur vers un objet d'administration de fournisseur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'objet d'administration du fournisseur a été renvoyé.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** pointé par _lpUID_ n'existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin:: AdminProviders** fournit l'accès à un objet d'administration de fournisseur. Une administration de fournisseur est un objet qui prend en charge l'interface [IProviderAdmin](iprovideradminiunknown.md) et permet aux clients d'effectuer les opérations suivantes: 
  
- Ajouter des fournisseurs de services à un service de messagerie.
    
- Supprimer des fournisseurs de services d'un service de messagerie.
    
- Ouvrez les sections de profil.
    
- Accéder à la table du fournisseur de services de messagerie.
    
Les types de modifications qui peuvent être apportées à un service de messagerie alors que le profil est en cours d'utilisation dépendent du service de messagerie. Toutefois, la plupart des services de messagerie ne prennent pas en charge les modifications telles que l'ajout et la suppression de fournisseurs lorsque le profil est en cours d'utilisation.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer la structure **MAPIUID** du service de messagerie à administrer, récupérez la colonne de propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de messagerie dans la table de service de message. Pour plus d'informations, reportez-vous à la procédure décrite dans la méthode [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg. cpp  <br/> |CMsgServiceTableDlg:: OnDisplayItem  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin:: AdminProviders** pour ouvrir un objet d'administration de fournisseur pour un service.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

