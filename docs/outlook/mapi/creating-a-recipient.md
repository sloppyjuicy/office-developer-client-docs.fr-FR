---
title: Création d'un destinataire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e14430d1539b90e089a9dabe1315384050f3dd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332955"
---
# <a name="creating-a-recipient"></a>Création d'un destinataire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients créent des destinataires lorsqu'ils adressent des messages et lorsqu'ils ajoutent des entrées à des conteneurs de carnet d'adresses modifiables. MAPI propose trois méthodes pour créer des destinataires:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Appelez **IAddrBook:: CreateOneOff** lorsque vous créez des destinataires à utiliser pour adresser des messages. **CreateOneOff** crée un identificateur d'entrée unique mis en forme pour être associé à une adresse d'un type d'adresse particulier. Pour plus d'informations sur les identificateurs d'entrée uniques et uniques, consultez les [adresses ponctuelles](one-off-addresses.md) et les [identificateurs d'entrée ponctuelle](one-off-entry-identifiers.md).
  
Appelez **IAddrBook:: NewEntry** lorsque vous créez des destinataires pour adresser des messages ou pour ajouter à un conteneur. **NewEntry** possède trois paires de paramètres qui contiennent des identificateurs d'entrée. Ces paramètres sont décrits ci-dessous: 
  
|**Paire de paramètres**|**Description**|
|:-----|:-----|
| _cbEidContainer_ et _lpEidContainer_ <br/> |Identificateur d'entrée du conteneur dans lequel la nouvelle entrée doit être placée.  <br/> |
| _cbEidNewEntryTpl_ et _lpEidNewEntryTpl_ <br/> |Identificateur d'entrée du modèle à utiliser pour créer la nouvelle entrée.  <br/> |
| _lpcbEidNewEntry_ et _lppEidNewEntry_ <br/> |Identificateur d'entrée de la nouvelle entrée.  <br/> |
   
Pour créer un destinataire pour un message sortant, définissez _cbEidContainer_ sur zéro et _lpEidContainer_ sur null. **NewEntry** crée un destinataire avec un identificateur d'entrée conforme au format One-Off, le même type de destinataire généré par un appel à **IAddrBook:: CreateOneOff**. 
  
Pour créer un destinataire à insérer dans un conteneur particulier, définissez _lpEidContainer_ sur l'identificateur d'entrée du conteneur et _cbEidContainer_ sur le nombre d'octets dans l'identificateur d'entrée du conteneur. 
  
Pour utiliser un modèle afin de créer un destinataire, définissez _lpEidNewEntryTpl_ sur l'identificateur d'entrée du modèle à utiliser et _cbEidNewEntryTpl_ sur le nombre d'octets dans cet identificateur d'entrée. La plupart des conteneurs de carnet d'adresses modifiables prennent en charge un ou plusieurs modèles pour la création d'entrées d'un type particulier. Les modèles uniques sont généralement, mais pas toujours, des boîtes de dialogue. La saisie d'informations dans le modèle génère un destinataire avec une adresse correctement mise en forme pour le type. 
  
Obtenez l'identificateur d'entrée de modèle à partir de l'un des éléments suivants:
  
- Colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) dans la table ponctuelle du conteneur, accessible en appelant la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur et en spécifiant **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) comme la balise de propriété et IID_IMAPITable comme identificateur d'interface. 
    
- Propriétés **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) d'un fournisseur de carnets d'adresses qui contiennent les identificateurs d'entrée pour l'objet utilisateur de messagerie du fournisseur et modèles de liste de distribution. 
    
> [!NOTE]
> Ne confondez pas l'identificateur d'entrée d'un nouveau modèle d'entrée avec un autre type d'identificateur d'entrée appelé un identificateur de modèle. Un identificateur de modèle est utilisé uniquement par les fournisseurs pour gérer les entrées copiées à partir d'autres fournisseurs; Il n'est jamais utilisé par les clients et il n'est pas utilisé pour créer de nouvelles entrées. 
  
Pour permettre à l'utilisateur de déterminer le type d'entrée à créer, transmettez zéro pour _cbEidNewEntryTpl_ et null pour _lpEidNewEntryTpl_. Dans ce cas, **NewEntry** affiche une boîte de dialogue commune créée à partir de la table ponctuelle MAPI, une liste hiérarchique de tous les modèles pris en charge par chaque fournisseur de carnet d'adresses dans le profil. 
  
Lorsqu'un type d'adresse a été déterminé, soit par le paramètre du paramètre _lpEidNewEntryTpl_ , soit par une sélection effectuée par l'utilisateur à partir de l'affichage de la table ponctuelle, **NewEntry** affiche le modèle correspondant à l'aide de sa table d'affichage. Tous les nouveaux modèles d'entrée prennent en charge la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). 
  
Pour que **NewEntry** renvoie l'identificateur d'entrée de l'entrée créée, transmettez une adresse valide pour les paramètres _lpcbEidNewEntry_ et _lppEidNewEntry_ . MAPI place le nouvel identificateur d'entrée à l'adresse désignée par _lppEidNewEntry_ et le nombre d'octets du nouvel identificateur d'entrée à l'adresse désignée par _lpcbEidNewEntry_.
  
Appelez [IABContainer:: CreateEntry](iabcontainer-createentry.md) pour créer un destinataire et l'enregistrer dans un conteneur de carnet d'adresses particulier. Vous pouvez utiliser cette méthode uniquement avec des conteneurs modifiables (conteneurs dont l'indicateur AB_MODIFIABLE est défini dans leur propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Les fournisseurs de carnet d'adresses avec des conteneurs non modifiables ne prennent pas en charge cette méthode. Spécifiez l'identificateur d'entrée du modèle pour créer une entrée du type souhaité dans le paramètre _lpEntryID_ . 
  
Dans le paramètre _ulCreateFlags_ , spécifiez le type de vérification d'entrée en double obligatoire et indique si les nouvelles entrées doivent remplacer celles qui existent. Si **CreateEntry** ne parvient pas à créer un nouvel objet en raison de la vérification d'entrée en double imposée par le fournisseur, ne voyez pas une erreur ou un avertissement renvoyé. Dans ces conditions, les fournisseurs renvoient un code de réussite. 
  
Si vous travaillez directement avec un conteneur et que vous connaissez exactement les types d'adresses que le conteneur peut créer, vous pouvez appeler **IABContainer:: CreateEntry** et transmettre l'identificateur d'entrée pour le modèle approprié. Le fournisseur de carnet d'adresses définit certaines propriétés par défaut initiales; vous pouvez appeler **SetProps** pour définir d'autres personnes. L'utilisateur n'est jamais impliqué. 
  

