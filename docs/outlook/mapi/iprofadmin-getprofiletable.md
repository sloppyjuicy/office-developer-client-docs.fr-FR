---
title: IProfAdminGetProfileTable
description: IProfAdmin GetProfileTable permet d’accéder à la table de profils, une table qui contient des informations sur tous les profils disponibles.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
ms.openlocfilehash: 42b450ba01fcbbbf48c2463f48ad36b28a4fb2aa
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828289"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès à la table de profils, une table qui contient des informations sur tous les profils disponibles.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Toujours NULL.
    
 _lppTable_
  
> [out] Pointeur vers un pointeur vers la table de profils.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table de profils a été récupérée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::GetProfileTable** permet d’accéder à la table de profils, qui contient une ligne pour chaque profil disponible. Il n’y a que deux colonnes dans chaque ligne : le nom d’affichage du profil et un indicateur qui indique si le profil est la valeur par défaut. 
  
Les profils qui ont été supprimés ou qui sont utilisés mais qui ont été marqués pour suppression ne sont pas inclus dans la table de profils. La table de profils est statique ; les ajouts et suppressions de profils suivants ne sont pas reflétés dans la table. 
  
S’il n’existe aucun profil, **GetProfileTable** retourne une table avec zéro ligne. 
  
Pour plus d’informations sur la table de profils, consultez [Tables de profils](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI utilise la méthode **IProfAdmin::GetProfileTable** pour obtenir la table de profils à afficher dans une nouvelle boîte de dialogue. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

