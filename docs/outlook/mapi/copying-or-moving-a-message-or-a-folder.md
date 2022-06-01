---
title: Copie ou déplacement d’un message ou dossier
description: Décrit les quatre méthodes qu’un client peut utiliser pour copier ou déplacer un message ou un dossier dans Microsoft Outlook.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
ms.openlocfilehash: 1217aaf49d1c860c317b6e15bfaa541baabc8767
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817962"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Copie ou déplacement d’un message ou dossier
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut utiliser l’une des quatre méthodes pour copier ou déplacer un message ou un dossier :
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
En définissant les indicateurs et paramètres appropriés, **CopyTo** et **CopyProps** peuvent fonctionner comme **CopyFolder** ou **CopyMessages**. Tenez compte des problèmes suivants lors de la décision de la méthode à appeler :
  
- Copiez-vous ou déplacez-vous un dossier ou un message ?
    
- Que savez-vous du dossier ou du message à déplacer ou à copier ?
    
- Combien de propriétés du dossier ou du message seront déplacées ou copiées ?
    
Vous pouvez utiliser les méthodes **IMAPIProp** pour copier ou déplacer un dossier ou un message. **IMAPIFolder::CopyMessages** fonctionne uniquement avec les messages ; **IMAPIFolder::CopyFolder** fonctionne uniquement avec des dossiers. 
  
Alors que l’utilisation des méthodes **IMAPIFolder** ne nécessite aucune connaissance des propriétés prises en charge par le dossier ou le message à copier ou à déplacer, vous devez avoir des connaissances pour utiliser les méthodes **IMAPIProp** . Avec **IMAPIProp::CopyProps**, vous devez être en mesure de spécifier explicitement les propriétés du dossier ou du message que vous souhaitez copier ou déplacer. Avec **IMAPIProp::CopyTo**, sauf si vous souhaitez copier ou déplacer toutes les propriétés, vous devez spécifier explicitement celles qui doivent être exclues. Pour plus d’informations sur ces méthodes, consultez [Copie des propriétés MAPI](copying-mapi-properties.md).
  
Le nombre de propriétés à copier ou à déplacer peut affecter votre décision quant à la méthode à utiliser. Si vous copiez ou déplacez plusieurs messages, appelez **IMAPIFolder::CopyMessages**. Un autre choix consiste à appeler **IMAPIProp::CopyProps** pour copier uniquement la propriété **PR_CONTAINER_CONTENTS** du dossier ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). La procédure suivante montre comment utiliser **CopyMessages**. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Pour copier ou déplacer un ou plusieurs messages
  
1. Recherchez les identificateurs d’entrée valides pour les dossiers source et de destination.
    
2. Ouvrez ces dossiers en mode lecture/écriture en appelant [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMsgStore::OpenEntry](imsgstore-openentry.md) et en définissant l’indicateur MAPI_MODIFY. 
    
3. Vérifiez que le pointeur d’interface retourné par **OpenEntry** est un pointeur d’interface **IMAPIFolder** . Si ce n’est pas le cas, effectuez un cast en type LPMAPIFOLDER. 
    
4. Créez un tableau d’identificateurs d’entrée représentant un ou plusieurs messages à copier ou déplacer. 
    
5. Appelez **IMAPIFolder::CopyMessages** avec les indicateurs suivants définis : 
    
   - MESSAGE_MOVE, si vous souhaitez effectuer une opération de déplacement. 
    
   - MESSAGE_DIALOG et passez un handle de fenêtre dans le paramètre _ulUIParam_ , si vous souhaitez que le dossier affiche un indicateur de progression. 
    
6. Relâchez les pointeurs **IMAPIFolder** pour les dossiers source et de destination. 
    
Si vous souhaitez copier le contenu complet d’un dossier vers un autre dossier, appelez la méthode **IMAPIFolder::CopyFolder** ou **IMAPIProp::CopyTo** du dossier source. 
  
Pour copier quelques-unes des propriétés d’un dossier, appelez sa méthode **IMAPIProp::CopyProps** . Pour copier la plupart des propriétés d’un dossier, appelez **IMAPIProp::CopyTo**. 
  
Par exemple, si vous souhaitez copier les propriétés **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) d’un dossier, vous disposez des options suivantes :
  
- Appelez **IMAPIFolder::CopyFolder** pour copier toutes les propriétés du dossier, puis supprimez les propriétés indésirables du nouveau dossier. 
    
- Appelez **CopyTo** et excluez toutes les propriétés du dossier, à l’exception des **PR_DISPLAY_NAME** et **des PR_COMMENT**. 
    
- Appelez **CopyProps**, en passant **PR_DISPLAY_NAME** et **PR_COMMENT** dans le tableau Include. 
    
Dans ce cas, **CopyProps** est le meilleur choix, car il est destiné à être utilisé pour copier un petit ensemble de propriétés et est l’appel le plus simple à implémenter. 
  
Pour copier ou déplacer uniquement des propriétés de dossier, sans inclure de messages, appelez la méthode **IMAPIProp::CopyTo** du dossier et excluez les propriétés suivantes : 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Les méthodes de copie peuvent retourner S_OK, indiquant la réussite totale, MAPI_W_PARTIAL_COMPLETION, indiquant une réussite partielle ou une erreur. Si MAPI_W_PARTIAL_COMPLETION est retourné, utilisez la macro **HR_FAILED** pour accéder à une erreur plus spécifique. Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
  
Si vous copiez des messages d’un magasin de messages vers un autre et qu’Unicode n’est pas pris en charge par les deux, sachez que les informations peuvent être perdues en raison de la conversion de page de code. En règle générale, vous ne pouvez pas savoir si les magasins de messages prennent en charge un ou les deux formats, ce qui rend impossible la copie des propriétés de texte sous forme de chaînes ASCII ou de chaînes Unicode. Si vous prenez en charge Unicode, essayez d’effectuer une copie Unicode ; en cas d’échec avec la valeur d’erreur MAPI_E_BAD_CHARWIDTH, recourez à ASCII.
  

