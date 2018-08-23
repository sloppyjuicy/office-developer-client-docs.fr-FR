---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 36e0db77097178d2db7a11b1339d19ebb8c91f2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565325"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Copie une ou plusieurs entrées, les utilisateurs de messagerie en général ou des listes de distribution.
  
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
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode. Le paramètre _ulUIParam_ doit être égal à zéro si l’indicateur AB_NO_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression, ou valeur NULL. Si _lpProgress_ est NULL, un indicateur de progression doit être affiché à l’aide de l’objet de l’avancement fourni par MAPI par le biais de la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) . Le paramètre _lpProgress_ est ignoré si l’indicateur AB_NO_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’opération de copie est effectuée. Les indicateurs suivants peuvent être définis :
    
AB_NO_DIALOG 
  
> Supprime l’affichage d’un indicateur de progression. Si cet indicateur n’est pas défini, un indicateur de progression est affiché.
    
CREATE_CHECK_DUP_LOOSE 
  
> Indique qu’un niveau de vérification de l’entrée en double libre doit être effectué. L’implémentation de vérification de l’entrée en double en vrac est spécifique au fournisseur. Par exemple, un fournisseur peut définir une correspondance partielle, comme les deux entrées qui ont le même nom d’affichage.
    
CREATE_CHECK_DUP_STRICT 
  
> Indique qu’un niveau strict de vérification de l’entrée en double doit être effectué. L’implémentation de vérification stricte entrée en double est spécifique au fournisseur. Par exemple, un fournisseur peut définir une correspondance exacte comme les deux entrées qui ont à la fois le même nom et l’adresse de messagerie.
    
CREATE_REPLACE 
  
> Indique qu’une nouvelle entrée doit remplacer un s’il est déterminé que les deux sont des doublons.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’opération de copie a réussi.
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> L’opération de copie a réussi, mais un ou plusieurs des entrées pas peuvent être copié. Lorsque cette valeur est renvoyée, l’appel doit être traité comme étant réussi. Pour tester cette valeur, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IABContainer::CopyEntries** copie les entrées à partir du conteneur même ou un autre conteneur. Un appel à **CopyEntries** est fonctionnellement équivalent à l’appel suivant pour chaque entrée à copier : 
  
1. La méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) pour créer la nouvelle entrée. 
    
2. La méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour lire les propriétés à partir de l’entrée à copier. 
    
3. La méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour écrire des propriétés dans la nouvelle entrée. 
    
4. Méthode de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée pour effectuer une sauvegarde. 
    
5. Méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) de la nouvelle entrée fourniture de référence du conteneur. 
    
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Tous les conteneurs qui prennent en charge la méthode **IABContainer::CopyEntries** doivent être modifiables. Définir l’indicateur AB_MODIFIABLE de votre conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu’il est modifiable. 
  
À prendre en charge tous les indicateurs ; Toutefois, l’interprétation et l’utilisation de ces indicateurs est spécifique à l’implémentation — autrement dit, vous pouvez déterminer la signification de la sémantique des indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT dans le cadre de votre implémentation. Si vous ne pouvez pas ou ne déterminez pas si une entrée est un doublon, toujours autoriser l’entrée doit être copié. 
  
Si l’indicateur CREATE_REPLACE est défini, copiez toujours l’entrée indépendamment si CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT est défini et si l’entrée est un doublon. 
  
Si CREATE_REPLACE n’est pas définie et CREATE_CHECK_DUP_STRICT est défini, vérifiez les doublons. Si une entrée s’avère être un double, ne pas copier l’entrée. 
  
Vous n’avez pas besoin prendre en charge CREATE_REPLACE ; ne pas de prise en charge CREATE_REPLACE signifie que vous pouvez l’ignorer et toujours effectuer une copie. 
  
Renvoie l’avertissement MAPI_W_PARTIAL_COMPLETION se produit uniquement si une entrée non dupliquée ne peut pas être copiée. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Utilisez les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT pour indiquer au fournisseur comment vous souhaitez le conteneur d’effectuer la vérification de l’entrée en double. Si vous avez besoin d’avoir une entrée ajoutée qu’il s’agisse d’un doublon, ne pas définir une de ces indicateurs ou définir l’indicateur CREATE_REPLACE. CREATE_REPLACE indique que vous n’êtes pas si une entrée est un doublon ; vous souhaitez toujours remplacer l’entrée d’origine. 
  
## <a name="see-also"></a>Voir aussi



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

