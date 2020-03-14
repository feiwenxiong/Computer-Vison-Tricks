# Computer-Vison-Tricks
For beginner like me, accumulating is acclerating！ 积累就是加速

## Parser  
to interpret input argumetns (用来理解terminal 中的输入参数)
import parser 
* parser = argparse.AugumentParser(description='   ' )
* parser.add_argumetn('--help', help = ' ')
* parser = parser_arg(args)

## torch.load()
for load model加载模型  
* torch.load_state_dict('')  for load weights 加载权重参数
PS:
When you call torch.load() on a file which contains GPU tensors, those tensors will be loaded to GPU by default. You can call torch.load(.., map_location='cpu') and then load_state_dict() to avoid GPU RAM surge when loading a model checkpoint.
reference: https://pytorch.org/docs/stable/torch.html

## troch.cuda.is_available() 判断是否有cuda gpu
* -model.cuda()  move model to gpu -
* data.to()


## train and test 测试和训练
* default train
* mode.eval()  
to evaluate/ to test

## with torch.no_grad()  
requires_grad = Flase

## torch.permute([ , , ]) 
H,W,C ---> C,H,W 就是把channels 换位置

x = torch.randn(2, 3, 5)
x.size()
torch.Size([2, 3, 5])
x.permute(2, 0, 1).size()
torch.Size([5, 2, 3])

## cv2.cvtColor(img, cv2.COLOR_RGB2GBR)
CV default BGR while Numpy is RGB

## torch.unsqueeze(dim=0)
BGR -->[batch size,C,H,W]


## Procssing in NN 
optimizer.zero_grad() + optimizer.step() + scheduler.lr_scheduler + loss


## size of image

floor(  (n-f)+2padding +1)




