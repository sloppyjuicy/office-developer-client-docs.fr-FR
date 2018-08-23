---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4e2d4f76fe436fd18b439bbbb558b1169094b438
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589461"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Établissement d’un dossier comme destination pour les messages entrants d’une classe de message particulier.
  
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
  
> [in] Un pointeur vers la classe de message qui sera associé au nouveau dossier de réception. Si le paramètre _lpszMessageClass_ est défini sur NULL ou une chaîne vide, **SetReceiveFolder** définit la valeur par défaut recevoir de dossier pour la banque de messages. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte dans les chaînes dans le passé. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> La chaîne de classe de message est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, la chaîne de classe de message est au format ANSI.
    
 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du dossier à établir en tant que le dossier de réception. Si le paramètre _lpEntryID_ est défini sur NULL, **SetReceiveFolder** remplace actuel recevoir de dossier par défaut de la banque de messages. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Un dossier de réception a été établi.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::SetReceiveFolder** définit ou modifie le dossier de réception pour une classe de message particulier. Avec **SetReceiveFolder**, un client peut, à l’aide d’appels successifs, spécifiez un autre dossier pour chaque classe de message défini de réception ou spécifier que les messages entrants pour plusieurs classes de message toutes les atteindre le même dossier. Par exemple, un client peut avoir sa propre classe de messages arrivent dans son propre dossier. Une application de télécopie peut désigner un dossier dans lequel le fournisseur de banque place les télécopies entrantes et un autre dossier dans lequel le fournisseur met les télécopies sortantes.
  
Si une erreur se produit pendant l’appel à **SetReceiveFolder**, le paramètre de dossier de réception reste inchangé. 
  
Si **SetReceiveFolder** modifie le paramètre de dossier de réception avec _lpEntryID_ valeur NULL, indiquant que le dossier de réception par défaut doit être défini, **SetReceiveFolder** renvoie S_OK même si aucun paramètre existant pour le texte indiqué s’est produite classe de message. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI utilise la méthode **IMsgStore::SetReceiveFolder** pour définir un dossier sous le dossier de réception pour une classe de message particulier.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

