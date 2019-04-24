---
title: Adresses ponctuelles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e6bda55951d8df5c5da272750c631ec105b2ccf2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279635"
---
# <a name="one-off-addresses"></a>Adresses ponctuelles

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les adresses ponctuelles sont utilisées pour envoyer des messages à des destinataires uniques, qui n'ont pas d'entrée correspondante dans l'un des conteneurs de carnet d'adresses de la session. Les clients peuvent créer des adresses uniques lorsqu'ils ajoutent de nouvelles entrées dans le carnet d'adresses ou de nouveaux destinataires à la liste des destinataires d'un message sortant. Il est possible d'ajouter des adresses ponctuelles à n'importe quel conteneur pouvant être modifié.
  
Pour créer une adresse ponctuelle, les clients utilisent un modèle spécial contenant des contrôles d'édition pour entrer toutes les informations qui constituent une adresse ponctuelle. Les adresses ponctuelles, comme les adresses d'autres types, utilisent un format prédéfini. Le format d'adresse unique est défini par MAPI de la manière suivante:
  
`Display name[Address type:Email address]`
  
Ce format comporte six composants et des règles de guillemets. Les composants sont décrits dans le tableau suivant.
  
|**Composant**|**Utilisation**|**Description**|
|:-----|:-----|:-----|
|Nom unique (DN)  <br/> |Facultatif  <br/> |S'il n'est pas présent, **IAddrBook:: ResolveName** utilise la partie visible de l'adresse de messagerie comme nom d'affichage. Peut contenir des espaces. Pour plus d'informations, voir [IAddrBook:: ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Obligatoire  <br/> |Définit le début des informations de type et d'adresse.  <br/> |
|]  <br/> |Obligatoire  <br/> |Définit la fin des informations relatives au type et à l'adresse. Si un élément autre que le blanc suit ce caractère, l'entrée n'est pas traitée comme un destinataire personnalisé.  <br/> |
|Type d'adresse  <br/> |Obligatoire  <br/> |Type d'adresse; correspond à un format d'adresse spécifique. Pour plus d'informations, consultez la rubrique [types d'adresses MAPI](mapi-address-types.md).  <br/> |
|:  <br/> |Obligatoire  <br/> |Sépare le type d'adresse de l'adresse de messagerie.  <br/> |
|Adresse de messagerie  <br/> |Obligatoire  <br/> |Adresse du destinataire. Peut contenir des espaces.  <br/> |
   
MAPI utilise des jeux de caractères de citation spécifiques pour permettre aux adresses de contenir des caractères spéciaux tels que la virgule (,), le crochet gauche ([) et le signe deux-points (:) et certains caractères non typés tels que le retour chariot ou le saut de ligne ou tout autre équivalent hexadécimal. Le caractère de cotation est la barre oblique\)inverse (. Par conséquent, si les clients ou fournisseurs doivent insérer une barre oblique inverse dans une adresse, ils doivent le faire précèder\\par le caractère guillemet ("").
  
Les clients et les fournisseurs de services peuvent utiliser cette technique d'établissement de devis dans l'un des champs pouvant être tapés et non fixes. Par exemple, l'entrée suivante se traduit par Bill Lee comme nom d'affichage, MSPEER comme type d'adresse et \\billll\in comme adresse de messagerie:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Pour insérer des caractères spéciaux non typés, les clients et les fournisseurs de services utilisent un caractère de citation suivi d'un x et de deux chiffres hexadécimaux pour représenter leur équivalent hexadécimal. Par exemple, si une adresse est dotée d'un caractère non typé qui équivaut à un retour chariot (\0d) en hexadécimal, un client l'entre comme suit:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook:: ResolveName** analyse également automatiquement la plupart des adresses SMTP, en recherchant les adresses avec le format suivant: 
  
`XXX@YYY.ZZZ`

Bien que tous les formats RFC822 possibles ne soient pas gérés, cette analyse automatique est adaptée à la plupart des utilisateurs. **ResolveName** inclut cette fonctionnalité pour permettre aux utilisateurs d'entrer des adresses SMTP directement dans un message et de faire en sorte que ce message soit dirigé vers l'utilisateur Internet. Les composants XXX, YYY et ZZZ de l'adresse peuvent être un ou plusieurs caractères. L'arobase (@) ne peut pas être inclus dans les composants d'adresse XXX, YYY ou ZZZ et le composant YYY ne peut pas non plus inclure le point. Étant donné que les caractères suivants sont des caractères spéciaux dans des adresses SMTP, MAPI convertit automatiquement un nom complet contenant ces caractères en une adresse unique: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Chaque adresse One-Off est assignée à un identificateur d'entrée unique correspondant. Pour effectuer cette attribution, les clients appellent **IAddrBook:: CreateOneOff** et les fournisseurs de transport **IMAPISupport:: CreateOneOff**. Pour plus d'informations, voir [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) et [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md). Lors du traitement des messages entrants, les fournisseurs de transport créent des identificateurs d'entrée uniques pour les adresses de passerelle et pour les adresses qui ne peuvent pas être gérées par les fournisseurs de carnet d'adresses associés au transport. Les fournisseurs de transport vérifient le type de chaque adresse dans un message afin de déterminer si elle peut être gérée par un fournisseur de carnet d'adresses associé au transport. Si ce n'est pas le cas, les fournisseurs de transport appellent **IMAPISupport:: CreateOneOff** pour associer l'adresse à un identificateur d'entrée unique. 
  
Les identificateurs d'entrée uniques incluent les informations suivantes dans l'ordre suivant:
  
1. **MAPIUID**
    
2. Version
    
3. Flags
    
4. Nom unique (DN)
    
5. Type d'adresse
    
6. Adresse de messagerie
    
Dans les appels à **IAddrBook:: CreateOneOff** et **IMAPISupport:: CreateOneOff**, les clients et les fournisseurs de transport peuvent définir un indicateur qui indique si le destinataire représenté par l'adresse unique peut traiter le texte mis en forme ou incorporé OLE objets. Pour indiquer qu'un destinataire peut gérer le texte mis en forme et les objets OLE, les clients et les fournisseurs de transport définissent l'indicateur MAPI_SEND_NO_RICH_INFO dans le paramètre _ulFlags_ . MAPI définit ensuite la propriété **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) du destinataire unique sur false. Lorsque cet indicateur n'est pas défini, MAPI affecte à **PR_SEND_RICH_INFO** la valeur true, sauf si l'adresse unique est interprétée comme une adresse SMTP. Dans ce cas, **PR_SEND_RICH_INFO** est défini sur false par défaut. 
  
## <a name="see-also"></a>Voir aussi

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

