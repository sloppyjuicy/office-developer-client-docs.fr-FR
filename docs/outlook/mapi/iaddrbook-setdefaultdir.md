---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783625"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**S’applique à**: Outlook 
  
Définit le conteneur spécifié par le conteneur de carnet d’adresses par défaut.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur de carnet d’adresses par défaut.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le conteneur de carnet d’adresses par défaut a été défini.
    
## <a name="remarks"></a>Remarques

Clients et fournisseurs de services appellent la méthode de **SetDefaultDir** pour établir un conteneur de carnet d’adresses par défaut nouveau. Le conteneur par défaut est le conteneur dans lequel l’utilisateur voit affiché dans le carnet d’adresses lors de la première ouverture du carnet d’adresses. **SetDefaultDir** enregistre le conteneur par défaut comme une entrée dans le profil. Le conteneur reste en tant que la valeur par défaut jusqu'à ce qu’un autre appel à **SetDefaultDir** est effectué dans la même session ou dans une autre session, soit le conteneur est supprimé. 
  
> [!NOTE]
> La propriété [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) correspond au paramètre **d’Accepter automatiquement** dans la boîte de dialogue Options de carnet d’adresses. Lorsque cette propriété existe dans la section profil [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) et est définie sur **true**, la boîte de dialogue Carnet d’adresses n’est plus le conteneur spécifié par **SetDefaultDir**par défaut, mais choisit un carnet d’adresses qui prend en compte Microsoft Outlook approprié pour le contexte dans lequel la boîte de dialogue a été affiché. Notez que cela peut entraîner une mauvaise expérience pour les fournisseurs de carnet d’adresses tiers. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI utilise la méthode **SetDefaultDir** pour effectuer le conteneur de carnet d’adresse spécifiée par défaut.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

