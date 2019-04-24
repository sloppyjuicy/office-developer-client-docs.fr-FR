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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334747"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une entrée de destinataire dont les données résident dans un fournisseur de carnet d'adresses hôte.
  
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
  
> dans Nombre d'octets dans l'identificateur de modèle pointé par le paramètre _lpTemplateID_ . 
    
 _lpTemplateID_
  
> dans Pointeur vers l'identificateur de modèle, ou propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), de l'entrée de destinataire à ouvrir.
    
 _ulTemplateFlags_
  
> dans Masque de des indicateurs utilisé pour indiquer comment ouvrir l'entrée représentée par l'identificateur de modèle. L'indicateur suivant peut être défini:
    
FILL_ENTRY 
  
> Le fournisseur hôte crée une entrée dans son conteneur en fonction de l'entrée représentée par l'identificateur de modèle. La méthode **IABLogon:: OpenTemplateID** doit effectuer une initialisation spécifique de l'entrée du fournisseur hôte à l'aide de l'implémentation [IMAPIProp: IUnknown](imapipropiunknown.md) dans le paramètre _LpMAPIPropData_ , ou renvoyer une **IMAPIProp personnalisée. **implémentation de l'interface dans le paramètre _lppMAPIPropNew_ . 
    
 _lpMAPIPropData_
  
> dans Pointeur vers l'objet Property du fournisseur hôte et l'implémentation d'une interface dérivée de **IMAPIProp**.
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente le type de pointeur d'interface à renvoyer dans le paramètre _lppMAPIPropNew_ . Le passage de la **valeur null** renvoie l'interface utilisateur de messagerie standard, [IMailUser: IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> remarquer Pointeur vers l'objet de propriété liée et implémentation d'une interface dérivée de **IMAPIProp**.
    
 _lpMAPIPropSibling_
  
> remarquer MSR doit être **null**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le code approprié a été correctement lié aux données connexes dans le fournisseur d'hôte.
    
MAPI_E_NO_SUPPORT 
  
> L'objet ne prend pas en charge les ID de modèle.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L'identificateur de modèle passé dans le paramètre _lpTemplateID_ n'est pas reconnu par le fournisseur de carnet d'adresses. 
    
## <a name="remarks"></a>Remarques

La méthode **IABLogon:: OpenTemplateID** est implémentée uniquement par les fournisseurs de carnet d'adresses qui doivent conserver le contrôle des copies de leurs entrées qui se trouvent dans les conteneurs des fournisseurs hôtes. Les fournisseurs qui implémentent **OpenTemplateID** sont appelés fournisseurs de carnets d'adresses étrangers. Les fournisseurs d'hôtes appellent [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) pour créer une entrée copiée ou ouvrir l'entrée copiée, et MAPI transmet l'appel à **IABLogon:: OpenTemplateID**. **IABLogon:: OpenTemplateID** ouvre l'entrée et lie le code qui le contrôle aux données du fournisseur hôte. 
  
Au lieu d'utiliser un identificateur d'entrée, **IABLogon:: OpenTemplateID** utilise une autre propriété, l'identificateur de modèle de l'entrée, **PR_TEMPLATEID**. Les identificateurs de modèle doivent être pris en charge pour les entrées dont le code doit être lié aux données dans un fournisseur d'hôte.
  
Voici quelques exemples de cas où un fournisseur de carnets d'adresses doit implémenter **IABLogon:: OpenTemplateID** sont les suivants: 
  
- Mettre à jour régulièrement les données d'une entrée copiée de sorte qu'elles restent synchronisées avec l'original.
    
- Implémenter les fonctionnalités que le fournisseur d'hôtes ne peut pas implémenter, telles que le remplissage dynamique d'une liste qui apparaît dans la table des détails de l'entrée à partir de données sur un serveur.
    
- Pour contrôler l'interaction entre les propriétés dans l'entrée du fournisseur de l'hôte et l'entrée d'origine, telles que le calcul de la **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) à partir des valeurs des contrôles d'édition dans l'affichage des détails qui contiennent différentes composants de l'adresse.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsqu'un fournisseur d'hôtes copie ou crée une entrée à partir de votre fournisseur et que vous fournissez une implémentation d'objet de propriété via **IABLogon:: OpenTemplateID**, vous gérez la plupart des appels pour maintenir l'entrée. Toutefois, étant donné qu'il revient au fournisseur hôte de transférer ces appels à vous, le fournisseur hôte peut intercepter tout appel et effectuer un traitement personnalisé avant de transférer l'appel.
  
Vous devez utiliser les instructions suivantes dans les implémentations de l'objet Property:
  
- Lorsque [IMAPIProp:: GetProps](imapiprop-getprops.md) est appelé, déterminez si la demande concerne une propriété calculée et, si c'est le cas, gérez-la. Transférez toutes les demandes pour les propriétés qui ne sont pas calculées vers le fournisseur hôte. 
    
- Lorsque [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) est appelé pour ouvrir une table à l'exception de la table d'affichage des détails, gérez la demande. La plupart des tables ne peuvent pas être copiées correctement sur le fournisseur hôte. Vous devez générer l'implémentation de l' **IMAPITable** pour ces tables demandées. La propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) de la table des détails doit être copiée sur le fournisseur hôte. Cela permet à ce fournisseur de générer la table localement. Vous souhaiterez peut-être encapsuler l'implémentation de la table d'affichage pour générer des notifications de table d'affichage. 
    
- Lorsque [IMAPIProp:: SetProps](imapiprop-setprops.md) est appelé, le fournisseur d'hôtes peut valider les données avant de vous permettre de définir les propriétés. Vous pouvez vérifier que toutes les propriétés nécessaires ont été définies ou calculées. Si une erreur est détectée, renvoyer la valeur d'erreur appropriée et, si possible, une explication supplémentaire via [IMAPIProp:: GetLastError](imapiprop-getlasterror.md).
    
- Lorsque [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) est appelé, le fournisseur hôte peut souhaiter effectuer un traitement avant l'enregistrement de l'entrée. Vous devez enregistrer toutes les données affectées par les propriétés modifiées, telles qu'une nouvelle adresse, dans l'entrée du fournisseur de l'hôte. 
    
En règle générale, votre implémentation de l'entrée que vous transmettez au fournisseur hôte interceptez toutes les méthodes pour effectuer une manipulation propre au contexte des propriétés pertinentes. Si l'indicateur FILL_ENTRY est transmis dans le paramètre _ulTemplateFlags_ , définissez toutes les propriétés de l'entrée. 
  
Si vous renvoyez un nouvel objet Property dans le paramètre _lppMAPIPropNew_ , appelez la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de l'objet Property du fournisseur hôte pour maintenir une référence. Tous les appels par le biais de l'objet lié que l'implémentation **IMAPIProp** a renvoyé dans _lppMAPIPropNew_ doivent être routés vers leur méthode correspondante dans l'objet de propriété hôte après qu'ils ont été traités par l'objet lié. 
  
Les identificateurs de propriété de toutes les propriétés nommées transmises via votre objet de propriété liée se trouvent dans l'espace de noms de l'identificateur de votre fournisseur. Votre implémentation de la méthode [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) doit déterminer les noms des propriétés afin qu'elle puisse effectuer des tâches spécifiques au modèle. De même, les propriétés que votre fournisseur transmet au fournisseur hôte doivent également figurer dans votre espace de noms. Par exemple, si vous définissez une propriété nommée dans **OpenTemplateID**, vous devez utiliser l'un de vos identificateurs pour le nom — en le créant, le cas échéant, en appelant la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
Si vous ne connaissez pas l'identificateur d'entrée passé dans _lpTemplateID_, renvoyez MAPI_E_UNKNOWN_ENTRYID.
  
Pour plus d'informations sur l'utilisation des identificateurs de modèle de carnet d'adresses, consultez la rubrique [agir en tant que fournisseur de carnet d'adresses étranger](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[Propriété canonique PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

