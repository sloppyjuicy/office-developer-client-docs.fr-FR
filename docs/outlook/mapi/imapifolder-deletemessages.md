---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280119"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un ou plusieurs messages.
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMsgList_
  
> dans Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient le nombre de messages à supprimer et un tableau de structures [EntryID](entryid.md) qui identifient les messages. 
    
 _ulUIParam_
  
> dans Handle de la fenêtre parent de l'indicateur de progression. Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> dans Pointeur vers un objet de progression qui affiche un indicateur de progression. Si la valeur NULL est transmise dans _lpProgress_, le fournisseur de banque de messages affiche un indicateur de progression à l'aide de l'implémentation de l'objet de progression MAPI. Le paramètre _lpProgress_ est ignoré sauf si l'indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont les messages sont supprimés. Les indicateurs suivants peuvent être définis:
    
DELETE_HARD_DELETE
  
> Supprime définitivement tous les messages, y compris ceux qui sont supprimés de manière récupérable.
    
MESSAGE_DIALOG 
  
> Affiche un indicateur de progression pendant l'exécution de l'opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le ou les messages spécifiés ont été supprimés.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L'appel a réussi, mais tous les messages n'ont pas été supprimés. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::D eletemessages** supprime les messages d'un dossier. Les messages qui n'existent pas, qui ont été déplacés ailleurs, qui sont ouverts avec une autorisation en lecture/écriture ou qui sont actuellement soumis, ne peuvent pas être supprimés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque l'opération de suppression implique plusieurs messages, effectuez l'opération aussi complètement que possible pour chaque dossier, même si un ou plusieurs messages ne peuvent pas être supprimés. N'arrêtez pas l'opération prématurément à moins qu'une défaillance ne se produise au-delà de votre contrôle, telle qu'une mémoire insuffisante, un manque d'espace disque ou une corruption de la Banque de messages.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoyée**|
|:-----|:-----|
|**DeleteMessages** a correctement supprimé tous les messages.  <br/> |S_OK  <br/> |
|**DeleteMessages** n'a pas pu supprimer tous les messages et sous-dossiers.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** n'a pas pu être exécuté.  <br/> |Toute valeur d'erreur à l'exception de MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **DeleteMessages** ne parvient pas à terminer, ne partez pas du principe qu'aucun travail n'a été effectué. **DeleteMessages** a peut-être pu supprimer un ou plusieurs messages avant de rencontrer l'erreur. 
  
 **DeleteMessages** renvoie MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l'implémentation de la Banque de messages. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::D eletemessages** pour supprimer les messages spécifiés.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ENTRÉE](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

