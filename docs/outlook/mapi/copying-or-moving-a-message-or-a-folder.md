---
title: Copie ou déplacement d’un message ou dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Dernière modification: 08 08, 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333039"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Copie ou déplacement d’un message ou dossier
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut utiliser l'une des quatre méthodes de copie ou de déplacement d'un message ou d'un dossier:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
En définissant les indicateurs et paramètres appropriés, **CopyTo** et **CopyProps** peuvent être configurés pour fonctionner comme **CopyFolder** ou **CopyMessages**. Tenez compte des points suivants lors du choix de la méthode à appeler:
  
- Est-ce que vous copiez ou déplacez un dossier ou un message?
    
- Dans quelle mesure le dossier ou le message doit-il être déplacé ou copié?
    
- Combien de propriétés du dossier ou du message seront déplacées ou copiées?
    
Vous pouvez utiliser les méthodes **IMAPIProp** pour copier ou déplacer un dossier ou un message. **IMAPIFolder:: CopyMessages** fonctionne avec les messages uniquement; **IMAPIFolder:: CopyFolder** ne fonctionne qu'avec des dossiers. 
  
Que l'utilisation des méthodes **IMAPIFolder** ne nécessite aucune connaissance des propriétés prises en charge par le dossier ou le message à copier ou déplacer, vous devez avoir des connaissances pour utiliser les méthodes **IMAPIProp** . Avec **IMAPIProp:: CopyProps**, vous devez être en mesure de spécifier explicitement les propriétés du dossier ou du message que vous souhaitez copier ou déplacer. Avec **IMAPIProp:: CopyTo**, sauf si vous souhaitez copier ou déplacer toutes les propriétés, vous devez explicitement spécifier celles qui doivent être exclues. Pour plus d'informations sur ces méthodes, reportez-vous à la rubrique [copie des propriétés MAPI](copying-mapi-properties.md).
  
Le nombre de propriétés à copier ou à déplacer peut affecter votre décision quant à la méthode à utiliser. Si vous copiez ou déplacez plusieurs messages, appelez **IMAPIFolder:: CopyMessages**. Une autre option consiste à appeler **IMAPIProp:: CopyProps** pour copier uniquement la propriété **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) du dossier. La procédure suivante montre comment utiliser **CopyMessages**. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Pour copier ou déplacer un ou plusieurs messages
  
1. Recherchez des identificateurs d'entrée valides pour les dossiers source et de destination.
    
2. Ouvrez ces dossiers en mode lecture/écriture en appelant [IMAPISession:: OpenEntry](imapisession-openentry.md) ou [IMsgStore:: OpenEntry](imsgstore-openentry.md) et en définissant l'indicateur MAPI_MODIFY. 
    
3. Vérifiez que le pointeur d'interface renvoyé depuis **OpenEntry** est un pointeur d'interface **IMAPIFolder** . Si ce n'est pas le cas, convertissez-le en type LPMAPIFOLDER. 
    
4. Créez un tableau d'identificateurs d'entrée représentant un ou plusieurs messages à copier ou déplacer. 
    
5. Appelez **IMAPIFolder:: CopyMessages** avec les indicateurs suivants: 
    
   - MESSAGE_MOVE, si vous voulez effectuer une opération de déplacement. 
    
   - MESSAGE_DIALOG et transmettez un descripteur de fenêtre dans le paramètre _ulUIParam_ , si vous souhaitez que le dossier affiche un indicateur de progression. 
    
6. Libérez les pointeurs **IMAPIFolder** pour les dossiers source et de destination. 
    
Si vous souhaitez copier l'intégralité du contenu d'un dossier dans un autre dossier, appelez la méthode **IMAPIFolder:: CopyFolder** ou **IMAPIProp:: CopyTo** du dossier source. 
  
Pour copier quelques-unes des propriétés d'un dossier, appelez sa méthode **IMAPIProp:: CopyProps** . Pour copier la plupart des propriétés d'un dossier, appelez **IMAPIProp:: CopyTo**. 
  
Par exemple, si vous souhaitez copier les propriétés **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) d'un dossier, vous disposez des options suivantes:
  
- Appelez **IMAPIFolder:: CopyFolder** pour copier toutes les propriétés du dossier, puis supprimez les propriétés indésirables du nouveau dossier. 
    
- Appelez **CopyTo** et excluez toutes les propriétés du dossier à l'exception de **PR_DISPLAY_NAME** et **PR_COMMENT**. 
    
- Appelez **CopyProps**, en passant **PR_DISPLAY_NAME** et **PR_COMMENT** dans le tableau include. 
    
Dans ce cas, **CopyProps** est le meilleur choix car il est destiné à être utilisé pour copier un petit ensemble de propriétés et est l'appel le plus simple à implémenter. 
  
Pour copier ou déplacer uniquement les propriétés de dossier, sans inclure les messages, appelez la méthode **IMAPIProp:: CopyTo** du dossier et excluez les propriétés suivantes: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Les méthodes Copy peuvent renvoyer S_OK, indiquant le total de la réussite, MAPI_W_PARTIAL_COMPLETION, indiquant la réussite partielle ou une erreur. Si MAPI_W_PARTIAL_COMPLETION est renvoyé, utilisez la macro **HR_FAILED** pour accéder à une erreur plus spécifique. Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
  
Si vous copiez des messages d'une banque de messages vers une autre et que Unicode n'est pas pris en charge par les deux, sachez que les informations peuvent être perdues en raison de la conversion de la page de codes. En règle générale, vous ne pouvez pas savoir si la Banque de messages prend en charge un ou les deux formats, ce qui empêche de déterminer s'il faut copier les propriétés de texte sous forme de chaînes ASCII ou Unicode. Si vous prenez en charge Unicode, essayez d'effectuer une copie Unicode; Si elle échoue avec la valeur d'erreur MAPI_E_BAD_CHARWIDTH, Resort to ASCII.
  

