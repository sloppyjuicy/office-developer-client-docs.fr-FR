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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b03245d7af4c6fb3879e597d8345e5d9888e164
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567208"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un pointeur qui fournit l’accès à un objet de l’administration du fournisseur.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique pour le service de message seront administrés. 
    
 _ulFlags_
  
> [in] Toujours NULL. 
    
 _lppProviderAdmin_
  
> [out] Pointeur vers un pointeur vers un objet d’administration de fournisseur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet de l’administration du fournisseur a été renvoyée avec succès.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** désignés par _lpUID_ n’existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::AdminProviders** permet d’accéder à un objet de l’administration du fournisseur. Administration du fournisseur est un objet qui prend en charge l’interface [IProviderAdmin](iprovideradminiunknown.md) et permet aux clients d’effectuer les opérations suivantes : 
  
- Ajouter des fournisseurs de services à un service de message.
    
- Supprimer les fournisseurs de services à partir d’un service de message.
    
- Ouvrez les sections du profil.
    
- Accéder à la table de fournisseur de service de message.
    
Les types de modifications pouvant être effectuées en réalité à un service de message alors que le profil est en cours d’utilisation dépendant du service de message. Toutefois, la plupart des services de messagerie n’acceptent pas les modifications telles que l’ajout et suppression de fournisseurs alors que le profil est en cours d’utilisation.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour récupérer la structure **MAPIUID** pour le service de message administrer, récupérez la colonne de la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table de service de message. Pour plus d’informations, voir la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::AdminProviders** pour ouvrir un objet d’administration de fournisseur d’un service.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

