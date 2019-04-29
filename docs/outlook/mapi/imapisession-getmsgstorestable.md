---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428136"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l'accès à la table de banque de messages qui contient des informations sur toutes les banques de messages dans le profil de session.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de réfixe des indicateurs qui déterminent le format des colonnes qui sont des chaînes de caractères. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les colonnes de chaîne sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes de la chaîne sont au format ANSI.
    
 _lppTable_
  
> remarquer Pointeur vers un pointeur vers la table de banque de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table a été renvoyée avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et la session ne prend pas en charge Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: GetMsgStoresTable** extrait un pointeur vers la table de banque de messages, une table gérée par MAPI qui contient des informations sur chaque banque de messages ouverte dans le profil. 
  
Pour obtenir la liste complète des colonnes obligatoires et facultatives dans la table de banque de messages, consultez la rubrique [tables des banques de messages](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Dans la mesure où MAPI met à jour la table de banque de messages pendant la session lorsque **** des modifications ont lieu, appelez la méthode Advise de la table de banque de messages pour vous inscrire afin d'être informé de ces modifications. Les modifications possibles incluent l'ajout de nouvelles banques de messages, la suppression de magasins existants et les modifications apportées à la Banque par défaut. 
  
La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable:: QueryColumns](imapitable-querycolumns.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md) . Cet indicateur contrôle également les types de propriétés dans l'ordre de tri retourné par la méthode [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnOpenMessageStoreTable  <br/> |MFCMAPI utilise la méthode **IMAPISession:: GetMsgStoresTable** pour obtenir la table de banque de messages afin qu'elle puisse être affichée dans la boîte de dialogue principale de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Tables de banque de messages](message-store-tables.md)

