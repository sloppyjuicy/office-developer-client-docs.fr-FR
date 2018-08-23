---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a8cd211cc16b620ac47357271070e0b45b867bea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579941"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Obtient le dossier qui a été établi comme dossier pour la banque de messages de réception de la destination pour les messages entrants d’une classe de message spécifié ou en tant que la valeur par défaut.
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>Paramètres

 _lpszMessageClass_
  
> [in] Pointeur vers une classe de message qui est associé à un dossier de réception. Si le paramètre _lpszMessageClass_ est défini sur NULL ou une chaîne vide, **GetReceiveFolder** renvoie la valeur par défaut recevoir de dossier pour la banque de messages. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes transmis et renvoyés. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> La chaîne de classe de message est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, la chaîne de classe de message est au format ANSI.
    
 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Un pointeur vers un pointeur vers l’identificateur d’entrée pour le dossier de réception.
    
 _lppszExplicitClass_
  
> [out] Un pointeur vers un pointeur vers la classe de message qui définit explicitement en tant que son dossier le dossier vers lequel pointe _lppEntryID_de réception. Cette classe de message doit être identique à la classe dans le paramètre _lpszMessageClass_ , ou une classe de base de cette classe. Valeur null indique que le dossier vers lequel pointé _lppEntryID_ est la valeur par défaut recevoir de dossier pour la banque de messages. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le dossier de réception a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::GetReceiveFolder** Obtient l’identificateur d’entrée d’un dossier de réception, un dossier désigné pour recevoir les messages entrants d’une classe de message particulier. Les appelants peuvent spécifier une classe de message ou la valeur NULL dans le paramètre _lpszMessageClass_ . Si _lpszMessageClass_ est NULL, **GetReceiveFolder** renvoie les valeurs suivantes : 
  
- Dans _lppszExplicitClass_, le nom de la classe de base du premier de la classe de message indiqué par _lpszMessageClass_ qui définit explicitement un dossier de réception. 
    
- Dans _lppEntryID_, l’identificateur d’entrée du dossier de réception pour la classe de base indiqué par le paramètre _lppszExplicitClass_ . 
    
Par exemple, supposons que le dossier de réception de la classe de message **IPM. Remarque** a été défini à l’entrée de l’identificateur de la boîte de réception et **GetReceiveFolder** est appelée avec le contenu de _lpszMessageClass_ définie sur **IPM. Note.Phone**. Si **IPM. Note.Phone** ne reçoit pas d’avoir explicite ensemble de dossiers, **GetReceiveFolder** renvoie l’identificateur d’entrée de la boîte de réception dans _lppEntryID_ et **IPM. Remarque** dans _lppszExplicitClass_.
  
Si le client appelle **GetReceiveFolder** pour une classe de message et n’a pas défini un dossier de réception pour cette classe de message, _lppszExplicitClass_ est une chaîne de longueur zéro, une chaîne au format Unicode ou une chaîne au format ANSI selon si la client définie l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ . 
  
Valeur par défaut réception dossier, obtenus en transmettant la valeur NULL dans le paramètre _lpszMessageClass_ , toujours existe pour chaque banque de messages. 
  
Un client doit appeler la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsqu’il est terminé avec l’identificateur d’entrée renvoyée dans _lppEntryID_ pour libérer de la mémoire qui contient l’identificateur d’entrée. Elle doit également appeler **MAPIFreeBuffer** lorsqu’il est terminé avec la chaîne de classe de message renvoyée dans _lppszExplicitClass_ pour libérer de la mémoire qui contient cette chaîne. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI utilise la méthode **IMsgStore::GetReceiveFolder** pour rechercher le dossier boîte de réception.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

