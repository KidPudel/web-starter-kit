some messing around with it:

```tsx
function App() {
  return (
    <div className='bg-[#FBA6BA] h-screen w-screen p-3'>
      <div className='border-4 border-black h-full w-full flex flex-col bg-[#A889FF]'>
        <h1 className=' flex justify-center items-center h-[50vh] text-green-300 bg-violet-500'>aa</h1>
        <h1 className=' flex justify-center items-center grow text-violet-500 bg-green-300'>aa</h1>

      </div>
    </div>
  );
}
```

will get us something like:
![image](https://user-images.githubusercontent.com/63263301/232208491-3d67111b-774d-4019-bbf9-0e48a356907e.png)
