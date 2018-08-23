---
title: Copier ou déplacer un message ou un dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Dernière modification : 08 novembre 2011'
ms.openlocfilehash: 97e7c90c2fdc715d7d0749300cc62854fffa6447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563981"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Copier ou déplacer un message ou un dossier
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un client peut utiliser un des quatre méthodes pour copier ou déplacer un message ou un dossier :
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
En définissant les paramètres et les indicateurs appropriés, **CopyTo** et **CopyProps** peuvent être effectuées de fonctionner comme **CopyFolder** ou **CopyMessages**. Lorsque vous décidez de la méthode à appeler, tenez compte des points suivants :
  
- Vous copiez ou déplacez un dossier ou un message ?
    
- Combien savoir sur le dossier ou le message d’être déplacé ou copié ?
    
- Combien de dossier ou les propriétés du message seront déplacées ou copiées ?
    
Vous pouvez utiliser les méthodes **IMAPIProp** pour copier ou déplacer un dossier ou un message. **IMAPIFolder::CopyMessages** fonctionne avec des messages uniquement ; **IMAPIFolder::CopyFolder** fonctionne avec les dossiers uniquement. 
  
Tandis que l’aide des méthodes **IMAPIFolder** ne nécessite pas de connaissances des propriétés prises en charge par le dossier ou le message à déplacer ou copier, vous devez avoir des connaissances d’utiliser les méthodes **IMAPIProp** . Avec **IMAPIProp::CopyProps**, vous devez être en mesure d’indiquer explicitement les propriétés de dossier ou un message que vous souhaitez copier ou déplacer. Avec **IMAPIProp::CopyTo**, sauf si vous souhaitez copier ou déplacer toutes les propriétés, vous devez explicitement spécifier ceux qui doit être exclus. Pour plus d’informations sur ces méthodes, voir la [Copie des propriétés MAPI](copying-mapi-properties.md).
  
Le nombre de propriétés à déplacer ou copier peut affecter votre décision quant à la méthode à utiliser. Si vous copiez ou déplacez plusieurs messages, appelez **IMAPIFolder::CopyMessages**. Un autre choix est d’appeler **IMAPIProp::CopyProps** pour copier uniquement la propriété **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) du dossier. La procédure suivante montre comment utiliser **CopyMessages**. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Pour copier ou déplacer un ou plusieurs messages
  
1. Recherchez les identificateurs d’entrée valide pour les dossiers source et de destination.
    
2. Ouvrez ces dossiers en mode lecture/écriture en appelant [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMsgStore::OpenEntry](imsgstore-openentry.md) et en définissant l’indicateur ne. 
    
3. Vérifiez que le pointeur d’interface retourné par **OpenEntry** est un pointeur d’interface **IMAPIFolder** . Si ce n’est pas le cas, effectuer un cast au type LPMAPIFOLDER. 
    
4. Créer un tableau d’identificateurs d’entrée représentant l’un ou plusieurs messages à déplacer ou copier. 
    
5. Appelez **IMAPIFolder::CopyMessages** avec l’ensemble d’indicateurs suivants : 
    
   - MESSAGE_MOVE, si vous souhaitez effectuer une opération de déplacement. 
    
   - MESSAGE_DIALOG et transmettre une fenêtre Gérer dans le paramètre _ulUIParam_ , si vous souhaitez que le dossier pour afficher un indicateur de progression. 
    
6. Libérer les pointeurs **IMAPIFolder** pour les dossiers source et de destination. 
    
Si vous souhaitez copier le contenu d’un dossier dans un autre dossier, appelez du dossier source **IMAPIFolder::CopyFolder** ou **IMAPIProp::CopyTo** . 
  
Pour copier quelques-unes des propriétés d’un dossier, appelez la méthode **IMAPIProp::CopyProps** . Pour copier la plupart des propriétés d’un dossier, appelez **IMAPIProp::CopyTo**. 
  
Par exemple, si vous souhaitez copier **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et les propriétés **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) d’un dossier, vous disposez des options suivantes :
  
- Appelez **IMAPIFolder::CopyFolder** pour copier toutes les propriétés de dossier, puis supprimer les indésirables dans le nouveau dossier. 
    
- Appelez **CopyTo** et exclure toutes les propriétés du dossier à l’exception **PR_DISPLAY_NAME** et **PR_COMMENT**. 
    
- Appelez **CopyProps**, en passant **PR_DISPLAY_NAME** et **PR_COMMENT** dans le tableau à inclure. 
    
Dans ce cas, **CopyProps** est recommandée, car il est destiné à être utilisé pour copier un petit jeu de propriétés et l’appel plus simple à implémenter. 
  
Pour copier ou déplacer uniquement les propriétés de dossier, sans inclure les messages, appelez la méthode de **IMAPIProp::CopyTo** du dossier et exclure les propriétés suivantes : 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Les méthodes de copie peuvent renvoyer S_OK, indiquant la réussite totale, MAPI_W_PARTIAL_COMPLETION se produit, indiquant la réussite partielle, ou une erreur. Si MAPI_W_PARTIAL_COMPLETION se produit est retourné, utilisez la macro **HR_FAILED** pour accéder à une erreur plus spécifique. Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
  
Si vous copiez des messages à partir d’une banque d’informations à un autre et Unicode n’est pas pris en charge par les deux, n’oubliez pas que les informations peuvent être perdues en raison de la conversion des pages de code. Vous ne peut pas savez généralement si les banques de messages prennent en charge les formats un ou les deux, ce qui empêche de déterminer s’il faut copier les propriétés de texte sous forme de chaînes ASCII ou en tant que chaînes Unicode. Si vous prenez en charge Unicode, essayez d’effectuer une copie Unicode ; Si elle échoue avec la valeur d’erreur MAPI_E_BAD_CHARWIDTH, recours à ASCII.
  

