---
title: IMsgServiceAdminAdminProviders
description: IMsgServiceAdminAdminProviders retourne un pointeur qui fournit l’accès à un objet d’administration de fournisseur.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
ms.openlocfilehash: 3cf379afc3d8bc2c07b03bc8957c7a18205d251f
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828379"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne un pointeur qui fournit l’accès à un objet d’administration de fournisseur.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message à administrer. 
    
 _ulFlags_
  
> [in] Toujours NULL. 
    
 _lppProviderAdmin_
  
> [out] Pointeur vers un pointeur vers un objet d’administration de fournisseur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet d’administration du fournisseur a été retourné avec succès.
    
MAPI_E_NOT_FOUND 
  
> Le **MAPIUID** pointé par  _lpUID_ n’existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::AdminProviders** fournit l’accès à un objet d’administration de fournisseur. Une administration de fournisseur est un objet qui prend en charge l’interface [IProviderAdmin](iprovideradminiunknown.md) et permet aux clients d’effectuer les opérations suivantes : 
  
- Ajoutez des fournisseurs de services à un service de message.
    
- Supprimez les fournisseurs de services d’un service de message.
    
- Ouvrez les sections de profil.
    
- Accédez à la table du fournisseur de services de message.
    
Les types de modifications qui peuvent être apportées à un service de message pendant l’utilisation du profil dépendent du service de message. Toutefois, la plupart des services de messages ne prennent pas en charge les modifications telles que l’ajout et la suppression de fournisseurs pendant l’utilisation du profil.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour récupérer la structure **MAPIUID** du service de message à administrer, récupérez la colonne de **propriétés PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table du service de messages. Pour plus d’informations, consultez la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::AdminProviders** pour ouvrir un objet d’administration de fournisseur pour un service. |
   
## <a name="see-also"></a>Voir aussi



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

