---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334747"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une entrée de destinataire dont les données résident dans un fournisseur de carnet d’adresses hôte.
  
```cpp
HRESULT OpenTemplateID(
  ULONG cbTemplateID,
  LPENTRYID lpTemplateID,
  ULONG ulTemplateFlags,
  LPMAPIPROP lpMAPIPropData,
  LPCIID lpInterface,
  LPMAPIPROP FAR * lppMAPIPropNew,
  LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Paramètres

 _cbTemplateID_
  
> [in] Nombre d’byte dans l’identificateur de modèle pointé par _le paramètre lpTemplateID._ 
    
 _lpTemplateID_
  
> [in] Pointeur vers l’identificateur de modèle, **ou PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), de l’entrée du destinataire à ouvrir.
    
 _ulTemplateFlags_
  
> [in] Masque de bits d’indicateurs utilisé pour indiquer comment ouvrir l’entrée représentée par l’identificateur de modèle. L’indicateur suivant peut être définie :
    
FILL_ENTRY 
  
> Le fournisseur d’hôte crée une entrée dans son conteneur en fonction de l’entrée représentée par l’identificateur de modèle. La méthode **IABLogon::OpenTemplateID** doit soit effectuer une initialisation spécifique de l’entrée du fournisseur hôte à l’aide de l’implémentation [IMAPIProp : IUnknown](imapipropiunknown.md) dans le paramètre _lpMAPIPropData,_ soit retourner une implémentation d’interface **IMAPIProp** personnalisée dans le paramètre _lppMAPIPropNew._ 
    
 _lpMAPIPropData_
  
> [in] Pointeur vers l’objet de propriété du fournisseur hôte et implémentation d’une interface dérivée **d’IMAPIProp**.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente le type de pointeur d’interface à retourner dans le paramètre _lppMAPIPropNew._ La **transmission de la** valeur null renvoie l’interface utilisateur de messagerie standard, [IMailUser : IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> [out] Pointeur vers l’objet de propriété liée et implémentation d’une interface dérivée **d’IMAPIProp**.
    
 _lpMAPIPropSibling_
  
> [out] Réservé ; doit être **null**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le code approprié a été lié aux données associées dans le fournisseur d’hôte.
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne prend pas en charge les ID de modèle.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur de modèle transmis dans  _le paramètre lpTemplateID_ n’est pas reconnu par le fournisseur de carnet d’adresses. 
    
## <a name="remarks"></a>Remarques

La **méthode IABLogon::OpenTemplateID** est implémentée uniquement par les fournisseurs de carnets d’adresses qui doivent contrôler les copies de leurs entrées situées dans les conteneurs de fournisseurs d’hôtes. Les fournisseurs qui **implémentent OpenTemplateID** sont appelés fournisseurs de carnet d’adresses étrangers. Les fournisseurs d’hôtes appellent [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour créer une entrée copiée ou ouvrir l’entrée copiée, et MAPI transmet l’appel à **IABLogon::OpenTemplateID**. **IABLogon::OpenTemplateID** ouvre l’entrée et lie le code qui la contrôle aux données du fournisseur hôte. 
  
Au lieu d’utiliser un identificateur d’entrée, **IABLogon::OpenTemplateID** utilise une autre propriété, l’identificateur de modèle de l’entrée, **PR_TEMPLATEID**. Les identificateurs de modèle doivent être pris en charge pour les entrées dont le code doit être lié à des données dans un fournisseur hôte.
  
Voici quelques exemples de cas où un fournisseur de carnet d’adresses doit implémenter **IABLogon::OpenTemplateID** : 
  
- Pour mettre à jour régulièrement les données d’une entrée copiée afin qu’elles restent synchronisées avec l’original.
    
- Pour implémenter des fonctionnalités que le fournisseur d’hôte ne peut pas implémenter, telles que le remplissage dynamique d’une liste qui apparaît dans la table de détails de l’entrée à partir de données sur un serveur.
    
- Pour contrôler l’interaction entre les propriétés de l’entrée du fournisseur hôte et l’entrée d’origine, par exemple, calculer le **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) à partir des valeurs des contrôles d’édition dans l’affichage des détails qui contiennent différents composants de l’adresse.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsqu’un fournisseur d’hôtes copie ou crée une entrée à partir de votre fournisseur et que vous fournissez une implémentation d’objet de propriété via **IABLogon::OpenTemplateID**, vous traitez la plupart des appels pour maintenir l’entrée. Toutefois, étant donné que c’est au fournisseur d’hôte de vous les faire suivre, le fournisseur hôte peut intercepter n’importe quel appel et effectuer un traitement personnalisé avant de le faire.
  
Vous devez utiliser les instructions suivantes dans vos implémentations d’objets de propriété :
  
- Lorsque [IMAPIProp::GetProps](imapiprop-getprops.md) est appelé, déterminez si la demande est pour une propriété calculée et, si c’est le cas, traitez-la. Transférer toutes les demandes de propriétés non complexes au fournisseur d’hôtes. 
    
- Lorsque [IMAPIProp::OpenProperty](imapiprop-openproperty.md) est appelé pour ouvrir une table à l’exception de la table d’affichage des détails, traitez la demande. La plupart des tables ne peuvent pas être copiées avec précision dans le fournisseur d’hôtes. Vous devez générer **l’implémentation IMAPITable** pour ces tables demandées. La table de **détails PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) doit être copiée dans le fournisseur hôte. Cela permet à ce fournisseur de générer la table localement. Vous souhaitez peut-être encapsuler l’implémentation de la table d’affichage pour générer des notifications de tableau d’affichage. 
    
- Lorsque [IMAPIProp::SetProps](imapiprop-setprops.md) est appelé, le fournisseur hôte peut valider les données avant de vous laisser définir les propriétés. Vous pouvez vérifier que toutes les propriétés nécessaires ont été définies ou calculées. Si une erreur est détectée, renvoyez la valeur d’erreur appropriée et, si possible, toute explication supplémentaire via [IMAPIProp::GetLastError](imapiprop-getlasterror.md).
    
- Lorsque [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelé, le fournisseur d’hôtes peut vouloir effectuer le traitement avant d’enregistrer l’entrée. Vous devez enregistrer toutes les données affectées par les propriétés modifiées, telles qu’une nouvelle adresse, dans l’entrée du fournisseur hôte. 
    
En règle générale, faites en sorte que votre implémentation de l’entrée que vous revoyez au fournisseur hôte intercepte toutes les méthodes pour effectuer une manipulation spécifique du contexte des propriétés pertinentes. Si l FILL_ENTRY est transmis dans le  _paramètre ulTemplateFlags,_ définissez toutes les propriétés de l’entrée. 
  
Si vous renvoyez un nouvel objet de propriété dans le paramètre  _lppMAPIPropNew,_ appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de l’objet de propriété du fournisseur hôte pour conserver une référence. Tous les appels via l’objet lié renvoyé par l’implémentation **IMAPIProp** dans  _lppMAPIPropNew_ doivent être acheminés vers leur méthode correspondante dans l’objet de propriété hôte une fois traités par l’objet lié. 
  
Les identificateurs de propriétés de toutes les propriétés nommées qui sont transmises via votre objet de propriété liée sont dans l’espace de noms d’identificateur de votre fournisseur. Votre implémentation de la méthode [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) doit déterminer les noms des propriétés afin qu’elle puisse effectuer toutes les tâches spécifiques au modèle. De même, les propriétés que votre fournisseur transmet au fournisseur hôte doivent également se trouver dans votre espace de noms. Par exemple, si vous définissez une propriété nommée dans **OpenTemplateID,** vous devez utiliser l’un de vos identificateurs pour le nom, en la créant, si nécessaire, en appelant la méthode [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) 
  
Si vous ne reconnaissez pas l’identificateur d’entrée transmis  _dans lpTemplateID_, renvoyez MAPI_E_UNKNOWN_ENTRYID.
  
Pour plus d’informations sur l’emploi des identificateurs de modèles de carnet d’adresses, voir Agir en tant que fournisseur de carnet [d’adresses étranger.](acting-as-a-foreign-address-book-provider.md)
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[Propriété canonique PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

