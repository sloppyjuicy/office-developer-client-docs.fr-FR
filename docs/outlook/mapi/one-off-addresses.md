---
title: Adresses ponctuelles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3deeda6441ae380b686b5038a59a2934c2255e9a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783844"
---
# <a name="one-off-addresses"></a>Adresses ponctuelles

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les adresses one-off sont utilisées pour envoyer des messages à des destinataires one-off, destinataires qui n’ont pas d’entrée correspondante dans l’un des conteneurs de carnet d’adresses de la session. Les clients peuvent créer des adresses one-off lorsqu’ils ajoutent de nouvelles entrées au carnet d’adresses ou de nouveaux destinataires à la liste des destinataires d’un message sortant. Des adresses non modifiables peuvent être ajoutées à n’importe quel conteneur.
  
Pour créer une adresse unique, les clients utilisent un modèle spécial contenant des contrôles de modification pour entrer toutes les informations qui constitue une adresse unique. Les adresses spécifiques, comme les adresses d’autres types, utilisent un format prédéféré. Le format d’adresse one-off est défini par MAPI comme suit :
  
`Display name[Address type:Email address]`
  
Il existe six composants pour ce format et certaines règles relatives au quoting des caractères. Les composants sont décrits dans le tableau suivant.
  
|**Composant**|**Utilisation**|**Description**|
|:-----|:-----|:-----|
|Nom d’affichage  <br/> |Facultatif  <br/> |S’il n’est pas présent, **IAddrBook::ResolveName** utilise la partie visible de l’adresse e-mail comme nom d’affichage. Peut inclure des espaces vides. Pour plus d’informations, [voir IAddrBook::ResolveName](iaddrbook-resolvename.md). |
|[  <br/> |Requis  <br/> |Définit le début des informations de type et d’adresse. |
|]  <br/> |Requis  <br/> |Définit la fin des informations de type et d’adresse. Si autre chose que l’espacement suit ce caractère, l’entrée n’est pas traitée comme un destinataire personnalisé. |
|Type d’adresse  <br/> |Requis  <br/> |Type d’adresse ; s’map après un format d’adresse spécifique. Pour plus d’informations, voir [Types d’adresse MAPI](mapi-address-types.md). |
|:  <br/> |Requis  <br/> |Sépare le type d’adresse de l’adresse de messagerie. |
|Adresse électronique  <br/> |Requis  <br/> |Adresse du destinataire. Peut inclure des espaces vides. |
   
MAPI utilise des jeux particuliers de caractères de quoting pour permettre aux adresses de contenir des caractères spéciaux tels que des virgules (,), des crochets gauches ([) et des deux-points (:) et certains caractères nontypes tels que le retour chariot ou le retour à la ligne ou tout autre équivalent hexadécimal. Le caractère de quoting est la barre oblique inverse (\). Par conséquent, si les clients ou les fournisseurs doivent insérer une barre oblique inverse dans une adresse, ils doivent la faire précéder du caractère de quoting (« \\ »).
  
Les clients et les fournisseurs de services peuvent utiliser cette technique de quoting dans n’importe quel champ nonfixé et typable. Par exemple, l’entrée suivante se traduit par Bill Lee comme nom d’affichage, MSPEER comme type \\d’adresse et billll\in comme adresse e-mail :
  
`Bill Lee[MSPEER:\\\\billl\in]`

Pour insérer des caractères spéciaux nontypes, les clients et les fournisseurs de services utilisent un caractère de quoting suivi d’un x et de deux chiffres hexadécimals pour représenter leur équivalent hexadécimal. Par exemple, si une adresse possède un caractère nontype qui équivaut à un retour chariot (\0d) en hexadécimal, un client les saisira comme :
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName** pare également automatiquement la plupart des adresses SMTP, en cherchant des adresses au format suivant : 
  
`XXX@YYY.ZZZ`

Bien que tous les formats RFC822 possibles ne soient pas gérés, cette recherche automatique est adaptée à la plupart des utilisateurs. **ResolveName inclut** cette fonctionnalité pour permettre aux utilisateurs d’entrer des adresses SMTP directement dans un message et d’envoyer ce message à l’utilisateur Internet. Les composants XXX, YYY et ZZZ de l’adresse peuvent être un ou plusieurs caractères. Le signe at (@) ne peut pas être inclus dans les composants d’adresse XXX, YYY ou ZZZ, et le composant YYY ne peut pas non plus inclure le point. Étant donné que les caractères suivants sont des caractères spéciaux dans les adresses SMTP, MAPI convertit automatiquement un nom complet contenant ces caractères en adresse un-off : 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Un identificateur d’entrée unique correspondant est affecté à chaque adresse unique. Pour effectuer cette affectation, les clients appellent **IAddrBook::CreateOneOff** et les fournisseurs de transport **appellent IMAPISupport::CreateOneOff**. Pour plus d’informations, voir [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) and [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Lors du traitement des messages entrants, les fournisseurs de transport créent des identificateurs d’entrée uniques pour les adresses de passerelle et pour les adresses qui ne peuvent pas être gérées par les fournisseurs de carnets d’adresses associés au transport. Les fournisseurs de transport vérifient le type de chaque adresse dans un message pour déterminer si elle peut être gérée par un fournisseur de carnet d’adresses associé au transport. Si ce n’est pas le cas, les fournisseurs de transport appellent **IMAPISupport::CreateOneOff** pour associer l’adresse à un identificateur d’entrée unique. 
  
Les identificateurs d’entrée uniques incluent les informations suivantes dans l’ordre suivant :
  
1. **MAPIUID**
    
2. Version
    
3. Flags
    
4. Nom d’affichage
    
5. Type d’adresse
    
6. Adresse électronique
    
Dans les appels à **IAddrBook::CreateOneOff** et **IMAPISupport::CreateOneOff**, les clients et les fournisseurs de transport peuvent définir un indicateur qui indique si le destinataire représenté par l’adresse one-off peut traiter du texte mis en forme ou des objets OLE incorporés. Pour indiquer qu’un destinataire peut gérer du texte mis en forme et des objets OLE, les clients et les fournisseurs de transport définissent l’indicateur MAPI_SEND_NO_RICH_INFO dans le paramètre _ulFlags_ . MAPI définit ensuite la propriété **PR_SEND_RICH_INFO (**[PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) du destinataire à FALSE. Lorsque cet indicateur n’est pas définie, MAPI définit **PR_SEND_RICH_INFO** sur TRUE, sauf si l’adresse one-off est interprétée comme une adresse SMTP. Dans ce cas, **la valeur PR_SEND_RICH_INFO** par défaut est FALSE. 
  
## <a name="see-also"></a>Voir aussi

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

