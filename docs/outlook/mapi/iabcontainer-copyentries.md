---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c0969e7518d2e326a35c2e37d8c94c3f6e97da27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580061"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une ou plusieurs entrées, généralement des utilisateurs de messagerie ou des listes de distribution.
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpEntries_
  
> [in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui contient les identificateurs d’entrée des entrées à copier. 
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode. Le _paramètre ulUIParam_ doit être zéro si l’AB_NO_DIALOG est définie dans _le paramètre ulFlags._ 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression, ou NULL. Si _lpProgress_ est NULL, un indicateur de progression doit être affiché à l’aide de l’objet de progression fourni par MAPI via la méthode [IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md) Le  _paramètre lpProgress est_ ignoré si l’AB_NO_DIALOG est définie dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le fonctionnement de l’opération de copie. Les indicateurs suivants peuvent être définies :
    
AB_NO_DIALOG 
  
> Supprime l’affichage d’un indicateur de progression. Si cet indicateur n’est pas définie, un indicateur de progression s’affiche.
    
CREATE_CHECK_DUP_LOOSE 
  
> Indique qu’un niveau souple de vérification des entrées en double doit être effectué. L’implémentation de la vérification des entrées libres en double est spécifique au fournisseur. Par exemple, un fournisseur peut définir une correspondance souple comme deux entrées qui ont le même nom d’affichage.
    
CREATE_CHECK_DUP_STRICT 
  
> Indique qu’un niveau strict de vérification des entrées en double doit être effectué. L’implémentation d’une vérification stricte des entrées en double est propre au fournisseur. Par exemple, un fournisseur peut définir une correspondance stricte comme deux entrées qui ont à la fois le même nom d’affichage et la même adresse de messagerie.
    
CREATE_REPLACE 
  
> Indique qu’une nouvelle entrée doit remplacer une entrée existante s’il est déterminé que les deux sont des doublons.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de copie a réussi.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’opération de copie a réussi globalement, mais une ou plusieurs des entrées n’ont pas pu être copiées. Lorsque cette valeur est renvoyée, l’appel doit être géré comme réussi. Pour tester cette valeur, utilisez la macro **HR_FAILED** macro. Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IABContainer::CopyEntries** copie les entrées du même conteneur ou d’un autre conteneur. Un appel à **CopyEntries équivaut** à effectuer les appels suivants pour chaque entrée à copier : 
  
1. Méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) pour créer la nouvelle entrée. 
    
2. La [méthode IMAPIProp::GetProps](imapiprop-getprops.md) pour lire les propriétés de l’entrée à copier. 
    
3. La [méthode IMAPIProp::SetProps](imapiprop-setprops.md) pour écrire des propriétés dans la nouvelle entrée. 
    
4. Méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée pour effectuer un enregistrement. 
    
5. Méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) de la nouvelle entrée pour libérer la référence du conteneur. 
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Tous les conteneurs qui la prise en charge de la méthode **IABContainer::CopyEntries** doivent être modifiables. Définissez l’indicateur AB_MODIFIABLE conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu’il est modifiable. 
  
Vous devez prendre en charge tous les indicateurs ; toutefois, l’interprétation et l’utilisation de ces indicateurs sont spécifiques à l’implémentation, c’est-à-dire que vous pouvez déterminer ce que signifient la sémantique des indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT dans le contexte de votre implémentation. Si vous ne pouvez pas ou ne déterminez pas si une entrée est en double, autorisez toujours la copie de l’entrée. 
  
Si l CREATE_REPLACE est définie, copiez toujours l’entrée, qu’elle soit CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT et qu’elle soit en double. 
  
Si CREATE_REPLACE n’est pas définie et CREATE_CHECK_DUP_STRICT est définie, recherchez les doublons. Si une entrée est déterminée comme dupliquée, ne copiez pas l’entrée. 
  
Vous n’avez pas besoin de prendre en charge CREATE_REPLACE; Ne pas prendre CREATE_REPLACE signifie que vous pouvez l’ignorer en toute sécurité et toujours effectuer une copie. 
  
Renvoyer l’avertissement MAPI_W_PARTIAL_COMPLETION uniquement si une entrée non mise en place ne peut pas être copiée. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Utilisez les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT pour indiquer au fournisseur comment vous souhaitez que le conteneur effectue la vérification des entrées en double. Si une entrée doit être ajoutée, qu’il s’agit d’un doublon ou non, ne définissez pas l’un de ces indicateurs ou définissez l’CREATE_REPLACE’indicateur. CREATE_REPLACE indique que vous ne vous souciez pas si une entrée est en double ; vous souhaitez toujours qu’elle remplace l’entrée d’origine. 
  
## <a name="see-also"></a>Voir aussi



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

