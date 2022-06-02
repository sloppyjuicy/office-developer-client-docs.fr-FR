---
title: IMsgStoreSetReceiveFolder
description: IMsgStore SetReceiveFolder établit un dossier comme destination pour les messages entrants d’une classe de message particulière.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
ms.openlocfilehash: a7d9c19db08394574c5266b6696c748fd4de7b5b
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828296"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit un dossier comme destination pour les messages entrants d’une classe de message particulière.
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpszMessageClass_
  
> [in] Pointeur vers la classe de message qui doit être associée au nouveau dossier de réception. Si le paramètre  _lpszMessageClass_ a la valeur NULL ou une chaîne vide, **SetReceiveFolder** définit le dossier de réception par défaut pour le magasin de messages. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type du texte dans les chaînes passées. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> La chaîne de classe de message est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, la chaîne de classe de message est au format ANSI.
    
 _cbEntryID_
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du dossier à établir en tant que dossier de réception. Si le paramètre  _lpEntryID_ est défini sur NULL, **SetReceiveFolder** remplace le dossier de réception actuel par la valeur par défaut du magasin de messages. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Un dossier de réception a été correctement établi.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::SetReceiveFolder** définit ou modifie le dossier de réception pour une classe de message particulière. Avec **SetReceiveFolder**, un client peut, à l’aide d’appels successifs, spécifier un dossier de réception différent pour chaque classe de message définie ou spécifier que les messages entrants pour plusieurs classes de messages sont tous placés dans le même dossier. Par exemple, un client peut avoir sa propre classe de messages arrivant dans son propre dossier. Une application de télécopie peut désigner un dossier dans lequel le fournisseur du magasin place les télécopies entrantes et un autre dossier dans lequel le fournisseur place les télécopies sortantes.
  
Si une erreur se produit pendant l’appel à **SetReceiveFolder**, le paramètre du dossier de réception reste inchangé. 
  
Si **SetReceiveFolder** modifie le paramètre de dossier de réception avec  _lpEntryID_ défini sur NULL, indiquant que le dossier de réception par défaut doit être défini, **SetReceiveFolder** retourne S_OK même s’il n’existe aucun paramètre existant pour la classe de message indiquée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI utilise la méthode **IMsgStore::SetReceiveFolder** pour définir un dossier comme dossier de réception pour une classe de message particulière. |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

